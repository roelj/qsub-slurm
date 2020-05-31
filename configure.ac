dnl Copyright © 2020 Roel Janssen <roel@gnu.org>
dnl
dnl This program is free software: you can redistribute it and/or modify
dnl it under the terms of the GNU General Public License as published by
dnl the Free Software Foundation, either version 3 of the License, or
dnl (at your option) any later version.
dnl
dnl This program is distributed in the hope that it will be useful,
dnl but WITHOUT ANY WARRANTY; without even the implied warranty of
dnl MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
dnl GNU General Public License for more details.
dnl
dnl You should have received a copy of the GNU General Public License
dnl along with this program. If not, see <http://www.gnu.org/licenses/>.
dnl -*- Autoconf -*-

AC_INIT([qsub-slurm], [0.0.2], [roel@gnu.org])
AM_INIT_AUTOMAKE([foreign])

GUILE_PKG([3.0 2.2 2.0])
GUILE_PROGS

dnl Test whether the "guile" command is somewhere in path.
dnl ---------------------------------------------------------------------------
if test "x$GUILE" = "x"; then
   AC_MSG_ERROR([Cannot find GNU Guile])
fi

dnl Test whether the "squeue" command is somewhere in path.
dnl ---------------------------------------------------------------------------
AC_PATH_PROG([SQUEUE], [squeue])
if test "x$SQUEUE" = "x"; then
   AC_MSG_ERROR([Cannot find squeue.])
fi

dnl Test whether the "sbatch" command is somewhere in path.
dnl ---------------------------------------------------------------------------
AC_PATH_PROG([SBATCH], [sbatch])
if test "x$SBATCH" = "x"; then
   AC_MSG_ERROR([Cannot find sbatch.])
fi

AC_CONFIG_FILES([Makefile])
AC_CONFIG_FILES([qsub], [chmod +x qsub])

AC_OUTPUT

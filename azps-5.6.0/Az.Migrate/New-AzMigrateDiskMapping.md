---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982781"
---
# <span data-ttu-id="34bce-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="34bce-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="34bce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34bce-102">SYNOPSIS</span></span>
<span data-ttu-id="34bce-103">Crea un nuovo mapping del disco</span><span class="sxs-lookup"><span data-stu-id="34bce-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="34bce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34bce-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="34bce-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34bce-105">DESCRIPTION</span></span>
<span data-ttu-id="34bce-106">Il cmdlet New-AzMigrateDiskMapping crea un mapping del disco di origine collegato al server di cui eseguire la migrazione</span><span class="sxs-lookup"><span data-stu-id="34bce-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="34bce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34bce-107">EXAMPLES</span></span>

### <span data-ttu-id="34bce-108">Esempio 1: Creare dischi</span><span class="sxs-lookup"><span data-stu-id="34bce-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="34bce-109">Ottenere l'oggetto disco per fornire l'input per New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="34bce-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="34bce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34bce-110">PARAMETERS</span></span>

### <span data-ttu-id="34bce-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="34bce-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="34bce-112">Specifica il set di encyption del disco da usare.</span><span class="sxs-lookup"><span data-stu-id="34bce-112">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34bce-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="34bce-113">-DiskID</span></span>
<span data-ttu-id="34bce-114">Specifica l'ID disco del disco collegato al server individuato di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="34bce-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34bce-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="34bce-115">-DiskType</span></span>
<span data-ttu-id="34bce-116">Specifica il tipo di dischi da usare per la macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="34bce-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34bce-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="34bce-117">-IsOSDisk</span></span>
<span data-ttu-id="34bce-118">Specifica se il disco contiene il sistema operativo per il server di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="34bce-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34bce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bce-119">CommonParameters</span></span>
<span data-ttu-id="34bce-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bce-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34bce-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bce-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="34bce-122">INPUTS</span></span>

## <span data-ttu-id="34bce-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34bce-123">OUTPUTS</span></span>

### <span data-ttu-id="34bce-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="34bce-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="34bce-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="34bce-125">NOTES</span></span>

<span data-ttu-id="34bce-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="34bce-126">ALIASES</span></span>

## <span data-ttu-id="34bce-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34bce-127">RELATED LINKS</span></span>


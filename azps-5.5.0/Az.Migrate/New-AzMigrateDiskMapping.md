---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203608"
---
# <span data-ttu-id="66955-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="66955-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="66955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66955-102">SYNOPSIS</span></span>
<span data-ttu-id="66955-103">Crea un nuovo mapping del disco</span><span class="sxs-lookup"><span data-stu-id="66955-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="66955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66955-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="66955-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="66955-105">DESCRIPTION</span></span>
<span data-ttu-id="66955-106">Il cmdlet New-AzMigrateDiskMapping crea un mapping del disco di origine collegato al server di cui eseguire la migrazione</span><span class="sxs-lookup"><span data-stu-id="66955-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="66955-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66955-107">EXAMPLES</span></span>

### <span data-ttu-id="66955-108">Esempio 1: Creare dischi</span><span class="sxs-lookup"><span data-stu-id="66955-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="66955-109">Ottenere l'oggetto disco per fornire l'input per New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="66955-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="66955-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66955-110">PARAMETERS</span></span>

### <span data-ttu-id="66955-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="66955-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="66955-112">Specifica il set di encyption del disco da usare.</span><span class="sxs-lookup"><span data-stu-id="66955-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="66955-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="66955-113">-DiskID</span></span>
<span data-ttu-id="66955-114">Specifica l'ID disco del disco collegato al server individuato di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="66955-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="66955-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="66955-115">-DiskType</span></span>
<span data-ttu-id="66955-116">Specifica il tipo di dischi da usare per la macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="66955-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66955-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="66955-117">-IsOSDisk</span></span>
<span data-ttu-id="66955-118">Specifica se il disco contiene il sistema operativo per il server di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="66955-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="66955-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66955-119">CommonParameters</span></span>
<span data-ttu-id="66955-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66955-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66955-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66955-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66955-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="66955-122">INPUTS</span></span>

## <span data-ttu-id="66955-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66955-123">OUTPUTS</span></span>

### <span data-ttu-id="66955-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="66955-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="66955-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="66955-125">NOTES</span></span>

<span data-ttu-id="66955-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="66955-126">ALIASES</span></span>

## <span data-ttu-id="66955-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66955-127">RELATED LINKS</span></span>


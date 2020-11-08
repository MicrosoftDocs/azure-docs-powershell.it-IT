---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202331"
---
# <span data-ttu-id="188e2-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="188e2-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="188e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="188e2-102">SYNOPSIS</span></span>
<span data-ttu-id="188e2-103">Crea un nuovo mapping del disco</span><span class="sxs-lookup"><span data-stu-id="188e2-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="188e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="188e2-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="188e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="188e2-105">DESCRIPTION</span></span>
<span data-ttu-id="188e2-106">Il cmdlet New-AzMigrateDiskMapping crea un mapping del disco di origine collegato al server di cui eseguire la migrazione</span><span class="sxs-lookup"><span data-stu-id="188e2-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="188e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="188e2-107">EXAMPLES</span></span>

### <span data-ttu-id="188e2-108">Esempio 1: creare dischi</span><span class="sxs-lookup"><span data-stu-id="188e2-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="188e2-109">Ottenere l'oggetto dischi per specificare l'input per New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="188e2-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="188e2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="188e2-110">PARAMETERS</span></span>

### <span data-ttu-id="188e2-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="188e2-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="188e2-112">Specifica il set di Encyption del disco da usare.</span><span class="sxs-lookup"><span data-stu-id="188e2-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="188e2-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="188e2-113">-DiskID</span></span>
<span data-ttu-id="188e2-114">Specifica l'ID disco del disco collegato al server individuato di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="188e2-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="188e2-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="188e2-115">-DiskType</span></span>
<span data-ttu-id="188e2-116">Specifica il tipo di dischi da usare per la VM di Azure.</span><span class="sxs-lookup"><span data-stu-id="188e2-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="188e2-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="188e2-117">-IsOSDisk</span></span>
<span data-ttu-id="188e2-118">Specifica se il disco contiene il sistema operativo per il server di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="188e2-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="188e2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188e2-119">CommonParameters</span></span>
<span data-ttu-id="188e2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188e2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188e2-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="188e2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188e2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="188e2-122">INPUTS</span></span>

## <span data-ttu-id="188e2-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="188e2-123">OUTPUTS</span></span>

### <span data-ttu-id="188e2-124">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="188e2-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="188e2-125">Note</span><span class="sxs-lookup"><span data-stu-id="188e2-125">NOTES</span></span>

<span data-ttu-id="188e2-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="188e2-126">ALIASES</span></span>

## <span data-ttu-id="188e2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="188e2-127">RELATED LINKS</span></span>


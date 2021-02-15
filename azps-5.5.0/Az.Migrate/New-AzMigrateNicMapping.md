---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203588"
---
# <span data-ttu-id="85441-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="85441-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="85441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85441-102">SYNOPSIS</span></span>
<span data-ttu-id="85441-103">Crea un oggetto per aggiornare le proprietà NIC di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="85441-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="85441-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85441-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="85441-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85441-105">DESCRIPTION</span></span>
<span data-ttu-id="85441-106">Il New-AzMigrateNicMapping cmdlet crea un mapping della scheda NIC di origine collegata al server di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="85441-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="85441-107">Questo oggetto viene fornito come input del cmdlet Set-AzMigrateServerReplication per aggiornare la scheda di rete e le relative proprietà per un server di replica.</span><span class="sxs-lookup"><span data-stu-id="85441-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="85441-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85441-108">EXAMPLES</span></span>

### <span data-ttu-id="85441-109">Esempio 1: Creare un oggetto NIC</span><span class="sxs-lookup"><span data-stu-id="85441-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="85441-110">Crea un oggetto di aggiornamento NIC.</span><span class="sxs-lookup"><span data-stu-id="85441-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="85441-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85441-111">PARAMETERS</span></span>

### <span data-ttu-id="85441-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="85441-112">-NicID</span></span>
<span data-ttu-id="85441-113">Specifica l'ID della scheda di rete da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="85441-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="85441-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="85441-114">-TargetNicIP</span></span>
<span data-ttu-id="85441-115">Specifica l'indirizzo IP all'interno della subnet di destinazione da usare per il nic.</span><span class="sxs-lookup"><span data-stu-id="85441-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="85441-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="85441-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="85441-117">Specifica se la scheda NIC da aggiornare sarà primaria, secondaria o non migrata.</span><span class="sxs-lookup"><span data-stu-id="85441-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="85441-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="85441-118">-TargetNicSubnet</span></span>
<span data-ttu-id="85441-119">Specifica il nome della subnet per il nic nella rete virtuale di destinazione in cui deve essere eseguita la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="85441-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="85441-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85441-120">CommonParameters</span></span>
<span data-ttu-id="85441-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85441-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85441-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85441-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85441-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="85441-123">INPUTS</span></span>

## <span data-ttu-id="85441-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85441-124">OUTPUTS</span></span>

### <span data-ttu-id="85441-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="85441-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="85441-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="85441-126">NOTES</span></span>

<span data-ttu-id="85441-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="85441-127">ALIASES</span></span>

## <span data-ttu-id="85441-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85441-128">RELATED LINKS</span></span>


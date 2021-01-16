---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: e0ce7e46e8105048d58ee8a4334eaf098b40399c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377884"
---
# <span data-ttu-id="05aac-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="05aac-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="05aac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05aac-102">SYNOPSIS</span></span>
<span data-ttu-id="05aac-103">Ottiene la risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="05aac-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="05aac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05aac-104">SYNTAX</span></span>

### <span data-ttu-id="05aac-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05aac-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05aac-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="05aac-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="05aac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05aac-107">DESCRIPTION</span></span>
<span data-ttu-id="05aac-108">Ottiene la risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="05aac-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="05aac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05aac-109">EXAMPLES</span></span>

### <span data-ttu-id="05aac-110">Esempio 1: ottenere informazioni dettagliate su tutte le risorse della raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="05aac-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM          

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.networ
                                          k/publicipaddresses/psdemovm-ip, /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psd
                                          emorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet, /subscriptions/e80eb9fa-c996-4435-aa32
                                          -5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemovm62
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : MovePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemovm62
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Network/networkInterfaces
ResourceSettingTargetResourceName       : psdemovm62
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network
                                          /networkInterfaces/psdemovm62
SourceResourceSettingResourceType       : Microsoft.Network/networkInterfaces
SourceResourceSettingTargetResourceName : psdemovm62
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemorm
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : CommitPending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemorm
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : resourceGroups
ResourceSettingTargetResourceName       : psdemorm2
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm
SourceResourceSettingResourceType       : resourceGroups
SourceResourceSettingTargetResourceName : psdemorm
Target                                  :
TargetId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psdemorm2
Type                                    :

```

<span data-ttu-id="05aac-111">Ottenere informazioni dettagliate su tutte le risorse della raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="05aac-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="05aac-112">Esempio 2: ottenere i dettagli di una specifica risorsa in una raccolta di mosse usando il nome della risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="05aac-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Name PSDemoVM   
                                                     
Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="05aac-113">Ottenere i dettagli di una specifica risorsa in una raccolta di mosse usando il nome della risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="05aac-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="05aac-114">Esempio 3: ottenere i dettagli di una specifica risorsa in una raccolta di mosse usando filtri come: SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="05aac-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Filter "Properties/SourceResourceName eq 'PSDemoVM'"

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="05aac-115">Ottenere i dettagli di una specifica risorsa in una raccolta di mosse tramite filtro, ad esempio Armid, moveStatusMoveState (verifica) e così via.</span><span class="sxs-lookup"><span data-stu-id="05aac-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="05aac-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05aac-116">PARAMETERS</span></span>

### <span data-ttu-id="05aac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05aac-117">-DefaultProfile</span></span>
<span data-ttu-id="05aac-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05aac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05aac-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="05aac-119">-Filter</span></span>
<span data-ttu-id="05aac-120">Il filtro da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="05aac-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="05aac-121">Ad esempio, puoi usare $filter = Properties/ProvisioningState EQ ' succeeded '.</span><span class="sxs-lookup"><span data-stu-id="05aac-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05aac-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="05aac-122">-MoveCollectionName</span></span>
<span data-ttu-id="05aac-123">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="05aac-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="05aac-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="05aac-124">-Name</span></span>
<span data-ttu-id="05aac-125">Il nome della risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="05aac-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05aac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05aac-126">-ResourceGroupName</span></span>
<span data-ttu-id="05aac-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05aac-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="05aac-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05aac-128">-SubscriptionId</span></span>
<span data-ttu-id="05aac-129">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="05aac-129">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05aac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05aac-130">CommonParameters</span></span>
<span data-ttu-id="05aac-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05aac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05aac-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05aac-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05aac-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05aac-133">INPUTS</span></span>

## <span data-ttu-id="05aac-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05aac-134">OUTPUTS</span></span>

### <span data-ttu-id="05aac-135">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="05aac-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="05aac-136">Note</span><span class="sxs-lookup"><span data-stu-id="05aac-136">NOTES</span></span>

<span data-ttu-id="05aac-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="05aac-137">ALIASES</span></span>

## <span data-ttu-id="05aac-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05aac-138">RELATED LINKS</span></span>


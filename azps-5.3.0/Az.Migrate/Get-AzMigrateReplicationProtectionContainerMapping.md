---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474081"
---
# <span data-ttu-id="43ce0-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="43ce0-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="43ce0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="43ce0-103">Ottiene i dettagli di un mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="43ce0-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="43ce0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43ce0-104">SYNTAX</span></span>

### <span data-ttu-id="43ce0-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43ce0-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43ce0-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="43ce0-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43ce0-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="43ce0-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="43ce0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43ce0-108">DESCRIPTION</span></span>
<span data-ttu-id="43ce0-109">Ottiene i dettagli di un mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="43ce0-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="43ce0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43ce0-110">EXAMPLES</span></span>

### <span data-ttu-id="43ce0-111">Esempio 1: ottenere un mapping specifico</span><span class="sxs-lookup"><span data-stu-id="43ce0-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="43ce0-112">Ottenere un dettaglio di mapping.</span><span class="sxs-lookup"><span data-stu-id="43ce0-112">Get a mapping detail.</span></span>

## <span data-ttu-id="43ce0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43ce0-113">PARAMETERS</span></span>

### <span data-ttu-id="43ce0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ce0-114">-DefaultProfile</span></span>
<span data-ttu-id="43ce0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43ce0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ce0-116">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="43ce0-116">-FabricName</span></span>
<span data-ttu-id="43ce0-117">Nome tessuto.</span><span class="sxs-lookup"><span data-stu-id="43ce0-117">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ce0-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="43ce0-118">-MappingName</span></span>
<span data-ttu-id="43ce0-119">Nome del mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="43ce0-119">Protection Container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ce0-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="43ce0-120">-ProtectionContainerName</span></span>
<span data-ttu-id="43ce0-121">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="43ce0-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ce0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ce0-122">-ResourceGroupName</span></span>
<span data-ttu-id="43ce0-123">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="43ce0-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="43ce0-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="43ce0-124">-ResourceName</span></span>
<span data-ttu-id="43ce0-125">Nome del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="43ce0-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="43ce0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43ce0-126">-SubscriptionId</span></span>
<span data-ttu-id="43ce0-127">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="43ce0-127">The subscription Id.</span></span>

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

### <span data-ttu-id="43ce0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ce0-128">CommonParameters</span></span>
<span data-ttu-id="43ce0-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ce0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ce0-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43ce0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ce0-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43ce0-131">INPUTS</span></span>

## <span data-ttu-id="43ce0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43ce0-132">OUTPUTS</span></span>

### <span data-ttu-id="43ce0-133">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="43ce0-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="43ce0-134">Note</span><span class="sxs-lookup"><span data-stu-id="43ce0-134">NOTES</span></span>

<span data-ttu-id="43ce0-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="43ce0-135">ALIASES</span></span>

## <span data-ttu-id="43ce0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43ce0-136">RELATED LINKS</span></span>


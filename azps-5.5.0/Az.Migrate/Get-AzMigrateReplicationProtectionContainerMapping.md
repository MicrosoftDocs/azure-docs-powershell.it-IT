---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 417f28feb03bbe55c787ff72021c2d9b16778cbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190159"
---
# <span data-ttu-id="5e545-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5e545-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="5e545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e545-102">SYNOPSIS</span></span>
<span data-ttu-id="5e545-103">Ottiene i dettagli di un mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="5e545-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="5e545-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e545-104">SYNTAX</span></span>

### <span data-ttu-id="5e545-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e545-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e545-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5e545-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e545-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="5e545-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e545-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e545-108">DESCRIPTION</span></span>
<span data-ttu-id="5e545-109">Ottiene i dettagli di un mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="5e545-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="5e545-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e545-110">EXAMPLES</span></span>

### <span data-ttu-id="5e545-111">Esempio 1: Ottenere un mapping specifico</span><span class="sxs-lookup"><span data-stu-id="5e545-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="5e545-112">Ottenere un dettaglio di mapping.</span><span class="sxs-lookup"><span data-stu-id="5e545-112">Get a mapping detail.</span></span>

## <span data-ttu-id="5e545-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e545-113">PARAMETERS</span></span>

### <span data-ttu-id="5e545-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e545-114">-DefaultProfile</span></span>
<span data-ttu-id="5e545-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e545-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e545-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="5e545-116">-FabricName</span></span>
<span data-ttu-id="5e545-117">Nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="5e545-117">Fabric name.</span></span>

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

### <span data-ttu-id="5e545-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="5e545-118">-MappingName</span></span>
<span data-ttu-id="5e545-119">Nome mapping contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="5e545-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="5e545-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="5e545-120">-ProtectionContainerName</span></span>
<span data-ttu-id="5e545-121">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="5e545-121">Protection container name.</span></span>

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

### <span data-ttu-id="5e545-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e545-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e545-123">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5e545-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="5e545-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5e545-124">-ResourceName</span></span>
<span data-ttu-id="5e545-125">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5e545-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="5e545-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e545-126">-SubscriptionId</span></span>
<span data-ttu-id="5e545-127">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="5e545-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="5e545-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e545-128">CommonParameters</span></span>
<span data-ttu-id="5e545-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e545-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e545-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e545-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e545-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e545-131">INPUTS</span></span>

## <span data-ttu-id="5e545-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e545-132">OUTPUTS</span></span>

### <span data-ttu-id="5e545-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5e545-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="5e545-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e545-134">NOTES</span></span>

<span data-ttu-id="5e545-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e545-135">ALIASES</span></span>

## <span data-ttu-id="5e545-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e545-136">RELATED LINKS</span></span>


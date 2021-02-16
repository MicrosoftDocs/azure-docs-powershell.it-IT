---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: fbee443cf8f24737ea6da78be347beac48d7e588
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190166"
---
# <span data-ttu-id="411dc-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="411dc-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="411dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="411dc-102">SYNOPSIS</span></span>
<span data-ttu-id="411dc-103">Ottiene i dettagli di un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="411dc-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="411dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="411dc-104">SYNTAX</span></span>

### <span data-ttu-id="411dc-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="411dc-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="411dc-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="411dc-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="411dc-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="411dc-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="411dc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="411dc-108">DESCRIPTION</span></span>
<span data-ttu-id="411dc-109">Ottiene i dettagli di un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="411dc-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="411dc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="411dc-110">EXAMPLES</span></span>

### <span data-ttu-id="411dc-111">Esempio 1: Elencare tutti i contenitori di protezione in vault e tessuto</span><span class="sxs-lookup"><span data-stu-id="411dc-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="411dc-112">Elenca tutto.</span><span class="sxs-lookup"><span data-stu-id="411dc-112">Lists all.</span></span>

### <span data-ttu-id="411dc-113">Esempio 2: Ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="411dc-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="411dc-114">Ne ottiene uno specifico.</span><span class="sxs-lookup"><span data-stu-id="411dc-114">Gets a specific one.</span></span>

## <span data-ttu-id="411dc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="411dc-115">PARAMETERS</span></span>

### <span data-ttu-id="411dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="411dc-116">-DefaultProfile</span></span>
<span data-ttu-id="411dc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="411dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="411dc-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="411dc-118">-FabricName</span></span>
<span data-ttu-id="411dc-119">Nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="411dc-119">Fabric name.</span></span>

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

### <span data-ttu-id="411dc-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="411dc-120">-ProtectionContainerName</span></span>
<span data-ttu-id="411dc-121">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="411dc-121">Protection container name.</span></span>

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

### <span data-ttu-id="411dc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411dc-122">-ResourceGroupName</span></span>
<span data-ttu-id="411dc-123">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="411dc-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="411dc-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="411dc-124">-ResourceName</span></span>
<span data-ttu-id="411dc-125">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="411dc-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="411dc-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="411dc-126">-SubscriptionId</span></span>
<span data-ttu-id="411dc-127">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="411dc-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="411dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411dc-128">CommonParameters</span></span>
<span data-ttu-id="411dc-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="411dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411dc-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="411dc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411dc-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="411dc-131">INPUTS</span></span>

## <span data-ttu-id="411dc-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="411dc-132">OUTPUTS</span></span>

### <span data-ttu-id="411dc-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="411dc-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="411dc-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="411dc-134">NOTES</span></span>

<span data-ttu-id="411dc-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="411dc-135">ALIASES</span></span>

## <span data-ttu-id="411dc-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="411dc-136">RELATED LINKS</span></span>


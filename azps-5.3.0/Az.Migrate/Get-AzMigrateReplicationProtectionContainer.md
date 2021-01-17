---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474084"
---
# <span data-ttu-id="987ee-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="987ee-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="987ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="987ee-102">SYNOPSIS</span></span>
<span data-ttu-id="987ee-103">Ottiene i dettagli di un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="987ee-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="987ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="987ee-104">SYNTAX</span></span>

### <span data-ttu-id="987ee-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="987ee-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="987ee-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="987ee-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="987ee-107">List1</span><span class="sxs-lookup"><span data-stu-id="987ee-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="987ee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="987ee-108">DESCRIPTION</span></span>
<span data-ttu-id="987ee-109">Ottiene i dettagli di un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="987ee-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="987ee-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="987ee-110">EXAMPLES</span></span>

### <span data-ttu-id="987ee-111">Esempio 1: elencare tutti i contenitori di protezione in Vault e in tessuto</span><span class="sxs-lookup"><span data-stu-id="987ee-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="987ee-112">Elenca tutti.</span><span class="sxs-lookup"><span data-stu-id="987ee-112">Lists all.</span></span>

### <span data-ttu-id="987ee-113">Esempio 2: ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="987ee-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="987ee-114">Ne ottiene uno specifico.</span><span class="sxs-lookup"><span data-stu-id="987ee-114">Gets a specific one.</span></span>

## <span data-ttu-id="987ee-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="987ee-115">PARAMETERS</span></span>

### <span data-ttu-id="987ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987ee-116">-DefaultProfile</span></span>
<span data-ttu-id="987ee-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="987ee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="987ee-118">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="987ee-118">-FabricName</span></span>
<span data-ttu-id="987ee-119">Nome tessuto.</span><span class="sxs-lookup"><span data-stu-id="987ee-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987ee-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="987ee-120">-ProtectionContainerName</span></span>
<span data-ttu-id="987ee-121">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="987ee-121">Protection container name.</span></span>

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

### <span data-ttu-id="987ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="987ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="987ee-123">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="987ee-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="987ee-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="987ee-124">-ResourceName</span></span>
<span data-ttu-id="987ee-125">Nome del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="987ee-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="987ee-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="987ee-126">-SubscriptionId</span></span>
<span data-ttu-id="987ee-127">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="987ee-127">The subscription Id.</span></span>

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

### <span data-ttu-id="987ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987ee-128">CommonParameters</span></span>
<span data-ttu-id="987ee-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987ee-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="987ee-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987ee-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="987ee-131">INPUTS</span></span>

## <span data-ttu-id="987ee-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="987ee-132">OUTPUTS</span></span>

### <span data-ttu-id="987ee-133">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="987ee-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="987ee-134">Note</span><span class="sxs-lookup"><span data-stu-id="987ee-134">NOTES</span></span>

<span data-ttu-id="987ee-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="987ee-135">ALIASES</span></span>

## <span data-ttu-id="987ee-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="987ee-136">RELATED LINKS</span></span>


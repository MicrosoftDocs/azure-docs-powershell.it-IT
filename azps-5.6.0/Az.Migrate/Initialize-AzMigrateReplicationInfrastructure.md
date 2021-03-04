---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982782"
---
# <span data-ttu-id="9c2ce-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="9c2ce-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="9c2ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2ce-103">Inizializza l'infrastruttura per il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="9c2ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c2ce-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c2ce-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="9c2ce-106">Il Initialize-AzMigrateReplicationInfrastructure di migrazione inizializza l'infrastruttura per il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="9c2ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c2ce-107">EXAMPLES</span></span>

### <span data-ttu-id="9c2ce-108">Esempio 1: Inizializza l'infrastruttura del progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="9c2ce-109">Inizializza l'infrastruttura per il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="9c2ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c2ce-110">PARAMETERS</span></span>

### <span data-ttu-id="9c2ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2ce-111">-DefaultProfile</span></span>
<span data-ttu-id="9c2ce-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c2ce-113">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="9c2ce-113">-ProjectName</span></span>
<span data-ttu-id="9c2ce-114">Specifica il nome del progetto di Azure Migrate da usare per la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="9c2ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c2ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c2ce-116">Specifica il gruppo di risorse del progetto Azure Migrate nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="9c2ce-117">-Scenario</span><span class="sxs-lookup"><span data-stu-id="9c2ce-117">-Scenario</span></span>
<span data-ttu-id="9c2ce-118">Specifica lo scenario di migrazione del server per cui deve essere inizializzata l'infrastruttura di replica.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="9c2ce-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c2ce-119">-SubscriptionId</span></span>
<span data-ttu-id="9c2ce-120">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-120">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ce-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="9c2ce-121">-TargetRegion</span></span>
<span data-ttu-id="9c2ce-122">Specifica l'area geografica di Azure di destinazione per le migrazioni del server.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="9c2ce-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c2ce-123">-Confirm</span></span>
<span data-ttu-id="9c2ce-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ce-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2ce-125">-WhatIf</span></span>
<span data-ttu-id="9c2ce-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c2ce-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2ce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2ce-128">CommonParameters</span></span>
<span data-ttu-id="9c2ce-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2ce-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2ce-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c2ce-131">INPUTS</span></span>

## <span data-ttu-id="9c2ce-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c2ce-132">OUTPUTS</span></span>

### <span data-ttu-id="9c2ce-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9c2ce-133">System.Boolean</span></span>

## <span data-ttu-id="9c2ce-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c2ce-134">NOTES</span></span>

<span data-ttu-id="9c2ce-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9c2ce-135">ALIASES</span></span>

## <span data-ttu-id="9c2ce-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c2ce-136">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207155"
---
# <span data-ttu-id="a0ca1-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="a0ca1-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="a0ca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ca1-103">Ottiene una soluzione nel progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="a0ca1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0ca1-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a0ca1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a0ca1-105">DESCRIPTION</span></span>
<span data-ttu-id="a0ca1-106">Ottiene una soluzione nel progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="a0ca1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0ca1-107">EXAMPLES</span></span>

### <span data-ttu-id="a0ca1-108">Esempio 1: Ottenere</span><span class="sxs-lookup"><span data-stu-id="a0ca1-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="a0ca1-109">Ottenere la migrazione della soluzione di progetto in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="a0ca1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0ca1-110">PARAMETERS</span></span>

### <span data-ttu-id="a0ca1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ca1-111">-DefaultProfile</span></span>
<span data-ttu-id="a0ca1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ca1-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="a0ca1-113">-MigrateProjectName</span></span>
<span data-ttu-id="a0ca1-114">Nome del progetto Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="a0ca1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a0ca1-115">-Name</span></span>
<span data-ttu-id="a0ca1-116">Nome univoco di una soluzione di migrazione all'interno di un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ca1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ca1-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0ca1-118">Il nome del gruppo di risorse di Azure di cui viene eseguita la migrazione fa parte del progetto.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="a0ca1-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0ca1-119">-SubscriptionId</span></span>
<span data-ttu-id="a0ca1-120">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="a0ca1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ca1-121">CommonParameters</span></span>
<span data-ttu-id="a0ca1-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ca1-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0ca1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ca1-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="a0ca1-124">INPUTS</span></span>

## <span data-ttu-id="a0ca1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0ca1-125">OUTPUTS</span></span>

### <span data-ttu-id="a0ca1-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="a0ca1-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="a0ca1-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="a0ca1-127">NOTES</span></span>

<span data-ttu-id="a0ca1-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a0ca1-128">ALIASES</span></span>

## <span data-ttu-id="a0ca1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0ca1-129">RELATED LINKS</span></span>


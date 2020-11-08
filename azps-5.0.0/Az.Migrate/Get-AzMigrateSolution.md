---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202333"
---
# <span data-ttu-id="fc23c-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="fc23c-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="fc23c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc23c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc23c-103">Ottiene una soluzione nel progetto migra.</span><span class="sxs-lookup"><span data-stu-id="fc23c-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="fc23c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc23c-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fc23c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc23c-105">DESCRIPTION</span></span>
<span data-ttu-id="fc23c-106">Ottiene una soluzione nel progetto migra.</span><span class="sxs-lookup"><span data-stu-id="fc23c-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="fc23c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc23c-107">EXAMPLES</span></span>

### <span data-ttu-id="fc23c-108">Esempio 1: ottenere</span><span class="sxs-lookup"><span data-stu-id="fc23c-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="fc23c-109">Ottenere la soluzione della migrazione del progetto per nome.</span><span class="sxs-lookup"><span data-stu-id="fc23c-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="fc23c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc23c-110">PARAMETERS</span></span>

### <span data-ttu-id="fc23c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc23c-111">-DefaultProfile</span></span>
<span data-ttu-id="fc23c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc23c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc23c-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="fc23c-113">-MigrateProjectName</span></span>
<span data-ttu-id="fc23c-114">Nome del progetto di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc23c-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="fc23c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc23c-115">-Name</span></span>
<span data-ttu-id="fc23c-116">Nome univoco di una soluzione di migrazione all'interno di un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="fc23c-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="fc23c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc23c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc23c-118">Il nome del gruppo di risorse di Azure in cui viene eseguita la migrazione di Project fa parte.</span><span class="sxs-lookup"><span data-stu-id="fc23c-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="fc23c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc23c-119">-SubscriptionId</span></span>
<span data-ttu-id="fc23c-120">ID sottoscrizione di Azure in cui è stata creata la migrazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="fc23c-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="fc23c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc23c-121">CommonParameters</span></span>
<span data-ttu-id="fc23c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc23c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc23c-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc23c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc23c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc23c-124">INPUTS</span></span>

## <span data-ttu-id="fc23c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc23c-125">OUTPUTS</span></span>

### <span data-ttu-id="fc23c-126">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180901Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="fc23c-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="fc23c-127">Note</span><span class="sxs-lookup"><span data-stu-id="fc23c-127">NOTES</span></span>

<span data-ttu-id="fc23c-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fc23c-128">ALIASES</span></span>

## <span data-ttu-id="fc23c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc23c-129">RELATED LINKS</span></span>


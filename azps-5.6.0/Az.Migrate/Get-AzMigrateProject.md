---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 4176b07f8a19538a05899b526d21f21cfcc20c9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982942"
---
# <span data-ttu-id="898d2-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="898d2-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="898d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="898d2-102">SYNOPSIS</span></span>
<span data-ttu-id="898d2-103">Metodo per eseguire la migrazione di un progetto.</span><span class="sxs-lookup"><span data-stu-id="898d2-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="898d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="898d2-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="898d2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="898d2-105">DESCRIPTION</span></span>
<span data-ttu-id="898d2-106">Metodo per eseguire la migrazione di un progetto.</span><span class="sxs-lookup"><span data-stu-id="898d2-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="898d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="898d2-107">EXAMPLES</span></span>

### <span data-ttu-id="898d2-108">Esempio 1: Ottenere</span><span class="sxs-lookup"><span data-stu-id="898d2-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="898d2-109">Metodo per eseguire la migrazione di un progetto.</span><span class="sxs-lookup"><span data-stu-id="898d2-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="898d2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="898d2-110">PARAMETERS</span></span>

### <span data-ttu-id="898d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898d2-111">-DefaultProfile</span></span>
<span data-ttu-id="898d2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="898d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="898d2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="898d2-113">-Name</span></span>
<span data-ttu-id="898d2-114">Nome del progetto Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="898d2-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="898d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898d2-115">-ResourceGroupName</span></span>
<span data-ttu-id="898d2-116">Il nome del gruppo di risorse di Azure di cui viene eseguita la migrazione fa parte del progetto.</span><span class="sxs-lookup"><span data-stu-id="898d2-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="898d2-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="898d2-117">-SubscriptionId</span></span>
<span data-ttu-id="898d2-118">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="898d2-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="898d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898d2-119">CommonParameters</span></span>
<span data-ttu-id="898d2-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="898d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898d2-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="898d2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898d2-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="898d2-122">INPUTS</span></span>

## <span data-ttu-id="898d2-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="898d2-123">OUTPUTS</span></span>

### <span data-ttu-id="898d2-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="898d2-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="898d2-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="898d2-125">NOTES</span></span>

<span data-ttu-id="898d2-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="898d2-126">ALIASES</span></span>

## <span data-ttu-id="898d2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="898d2-127">RELATED LINKS</span></span>


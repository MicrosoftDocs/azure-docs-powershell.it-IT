---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207162"
---
# <span data-ttu-id="6c43b-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="6c43b-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="6c43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c43b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c43b-103">Metodo per eseguire la migrazione di un progetto.</span><span class="sxs-lookup"><span data-stu-id="6c43b-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="6c43b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c43b-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6c43b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c43b-105">DESCRIPTION</span></span>
<span data-ttu-id="6c43b-106">Metodo per eseguire la migrazione di un progetto.</span><span class="sxs-lookup"><span data-stu-id="6c43b-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="6c43b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c43b-107">EXAMPLES</span></span>

### <span data-ttu-id="6c43b-108">Esempio 1: Ottenere</span><span class="sxs-lookup"><span data-stu-id="6c43b-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="6c43b-109">Metodo per eseguire la migrazione di un progetto.</span><span class="sxs-lookup"><span data-stu-id="6c43b-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="6c43b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c43b-110">PARAMETERS</span></span>

### <span data-ttu-id="6c43b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c43b-111">-DefaultProfile</span></span>
<span data-ttu-id="6c43b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c43b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c43b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6c43b-113">-Name</span></span>
<span data-ttu-id="6c43b-114">Nome del progetto Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="6c43b-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="6c43b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c43b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6c43b-116">Il nome del gruppo di risorse di Azure di cui viene eseguita la migrazione fa parte del progetto.</span><span class="sxs-lookup"><span data-stu-id="6c43b-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="6c43b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c43b-117">-SubscriptionId</span></span>
<span data-ttu-id="6c43b-118">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="6c43b-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="6c43b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c43b-119">CommonParameters</span></span>
<span data-ttu-id="6c43b-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c43b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c43b-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c43b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c43b-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c43b-122">INPUTS</span></span>

## <span data-ttu-id="6c43b-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c43b-123">OUTPUTS</span></span>

### <span data-ttu-id="6c43b-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="6c43b-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="6c43b-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c43b-125">NOTES</span></span>

<span data-ttu-id="6c43b-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6c43b-126">ALIASES</span></span>

## <span data-ttu-id="6c43b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c43b-127">RELATED LINKS</span></span>


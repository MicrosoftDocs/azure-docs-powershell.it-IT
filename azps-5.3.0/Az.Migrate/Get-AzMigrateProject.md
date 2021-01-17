---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474083"
---
# <span data-ttu-id="f40c2-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="f40c2-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="f40c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f40c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f40c2-103">Metodo per ottenere un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="f40c2-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="f40c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f40c2-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f40c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f40c2-105">DESCRIPTION</span></span>
<span data-ttu-id="f40c2-106">Metodo per ottenere un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="f40c2-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="f40c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f40c2-107">EXAMPLES</span></span>

### <span data-ttu-id="f40c2-108">Esempio 1: ottenere</span><span class="sxs-lookup"><span data-stu-id="f40c2-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="f40c2-109">Metodo per ottenere un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="f40c2-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="f40c2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f40c2-110">PARAMETERS</span></span>

### <span data-ttu-id="f40c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f40c2-111">-DefaultProfile</span></span>
<span data-ttu-id="f40c2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f40c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f40c2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f40c2-113">-Name</span></span>
<span data-ttu-id="f40c2-114">Nome del progetto di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f40c2-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="f40c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f40c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="f40c2-116">Il nome del gruppo di risorse di Azure in cui viene eseguita la migrazione di Project fa parte.</span><span class="sxs-lookup"><span data-stu-id="f40c2-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="f40c2-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f40c2-117">-SubscriptionId</span></span>
<span data-ttu-id="f40c2-118">ID sottoscrizione di Azure in cui è stata creata la migrazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="f40c2-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="f40c2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40c2-119">CommonParameters</span></span>
<span data-ttu-id="f40c2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f40c2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f40c2-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f40c2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40c2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f40c2-122">INPUTS</span></span>

## <span data-ttu-id="f40c2-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f40c2-123">OUTPUTS</span></span>

### <span data-ttu-id="f40c2-124">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="f40c2-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="f40c2-125">Note</span><span class="sxs-lookup"><span data-stu-id="f40c2-125">NOTES</span></span>

<span data-ttu-id="f40c2-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f40c2-126">ALIASES</span></span>

## <span data-ttu-id="f40c2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f40c2-127">RELATED LINKS</span></span>


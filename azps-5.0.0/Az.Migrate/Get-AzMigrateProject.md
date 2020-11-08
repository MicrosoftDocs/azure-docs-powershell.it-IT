---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203532"
---
# <span data-ttu-id="39121-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="39121-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="39121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39121-102">SYNOPSIS</span></span>
<span data-ttu-id="39121-103">Metodo per ottenere un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="39121-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="39121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39121-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="39121-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39121-105">DESCRIPTION</span></span>
<span data-ttu-id="39121-106">Metodo per ottenere un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="39121-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="39121-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39121-107">EXAMPLES</span></span>

### <span data-ttu-id="39121-108">Esempio 1: ottenere</span><span class="sxs-lookup"><span data-stu-id="39121-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="39121-109">Metodo per ottenere un progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="39121-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="39121-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39121-110">PARAMETERS</span></span>

### <span data-ttu-id="39121-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39121-111">-DefaultProfile</span></span>
<span data-ttu-id="39121-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39121-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39121-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="39121-113">-Name</span></span>
<span data-ttu-id="39121-114">Nome del progetto di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="39121-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="39121-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39121-115">-ResourceGroupName</span></span>
<span data-ttu-id="39121-116">Il nome del gruppo di risorse di Azure in cui viene eseguita la migrazione di Project fa parte.</span><span class="sxs-lookup"><span data-stu-id="39121-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="39121-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39121-117">-SubscriptionId</span></span>
<span data-ttu-id="39121-118">ID sottoscrizione di Azure in cui è stata creata la migrazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="39121-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="39121-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39121-119">CommonParameters</span></span>
<span data-ttu-id="39121-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39121-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39121-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39121-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39121-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39121-122">INPUTS</span></span>

## <span data-ttu-id="39121-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39121-123">OUTPUTS</span></span>

### <span data-ttu-id="39121-124">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="39121-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="39121-125">Note</span><span class="sxs-lookup"><span data-stu-id="39121-125">NOTES</span></span>

<span data-ttu-id="39121-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="39121-126">ALIASES</span></span>

## <span data-ttu-id="39121-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39121-127">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180207"
---
# <span data-ttu-id="c61f1-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="c61f1-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="c61f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c61f1-103">Metodo per ottenere un sito.</span><span class="sxs-lookup"><span data-stu-id="c61f1-103">Method to get a site.</span></span>

## <span data-ttu-id="c61f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c61f1-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c61f1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c61f1-105">DESCRIPTION</span></span>
<span data-ttu-id="c61f1-106">Metodo per ottenere un sito.</span><span class="sxs-lookup"><span data-stu-id="c61f1-106">Method to get a site.</span></span>

## <span data-ttu-id="c61f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c61f1-107">EXAMPLES</span></span>

### <span data-ttu-id="c61f1-108">Esempio 1: Ottieni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c61f1-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="c61f1-109">Ottenere il sito in base al nome</span><span class="sxs-lookup"><span data-stu-id="c61f1-109">Get site by name</span></span>

## <span data-ttu-id="c61f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c61f1-110">PARAMETERS</span></span>

### <span data-ttu-id="c61f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61f1-111">-DefaultProfile</span></span>
<span data-ttu-id="c61f1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c61f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c61f1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c61f1-113">-Name</span></span>
<span data-ttu-id="c61f1-114">Nome del sito.</span><span class="sxs-lookup"><span data-stu-id="c61f1-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c61f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="c61f1-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c61f1-116">The name of the resource group.</span></span>
<span data-ttu-id="c61f1-117">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c61f1-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c61f1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c61f1-118">-SubscriptionId</span></span>
<span data-ttu-id="c61f1-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c61f1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c61f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61f1-120">CommonParameters</span></span>
<span data-ttu-id="c61f1-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c61f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61f1-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c61f1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61f1-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="c61f1-123">INPUTS</span></span>

## <span data-ttu-id="c61f1-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c61f1-124">OUTPUTS</span></span>

### <span data-ttu-id="c61f1-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="c61f1-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="c61f1-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="c61f1-126">NOTES</span></span>

<span data-ttu-id="c61f1-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c61f1-127">ALIASES</span></span>

## <span data-ttu-id="c61f1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c61f1-128">RELATED LINKS</span></span>


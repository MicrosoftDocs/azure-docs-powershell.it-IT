---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475209"
---
# <span data-ttu-id="fcf75-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="fcf75-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="fcf75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcf75-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf75-103">Metodo per ottenere un sito.</span><span class="sxs-lookup"><span data-stu-id="fcf75-103">Method to get a site.</span></span>

## <span data-ttu-id="fcf75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcf75-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fcf75-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcf75-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf75-106">Metodo per ottenere un sito.</span><span class="sxs-lookup"><span data-stu-id="fcf75-106">Method to get a site.</span></span>

## <span data-ttu-id="fcf75-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcf75-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf75-108">Esempio 1: Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fcf75-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="fcf75-109">Ottenere il sito per nome</span><span class="sxs-lookup"><span data-stu-id="fcf75-109">Get site by name</span></span>

## <span data-ttu-id="fcf75-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcf75-110">PARAMETERS</span></span>

### <span data-ttu-id="fcf75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf75-111">-DefaultProfile</span></span>
<span data-ttu-id="fcf75-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf75-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcf75-113">-Name</span></span>
<span data-ttu-id="fcf75-114">Nome sito.</span><span class="sxs-lookup"><span data-stu-id="fcf75-114">Site name.</span></span>

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

### <span data-ttu-id="fcf75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf75-115">-ResourceGroupName</span></span>
<span data-ttu-id="fcf75-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fcf75-116">The name of the resource group.</span></span>
<span data-ttu-id="fcf75-117">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fcf75-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fcf75-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fcf75-118">-SubscriptionId</span></span>
<span data-ttu-id="fcf75-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fcf75-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fcf75-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf75-120">CommonParameters</span></span>
<span data-ttu-id="fcf75-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf75-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf75-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcf75-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf75-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcf75-123">INPUTS</span></span>

## <span data-ttu-id="fcf75-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcf75-124">OUTPUTS</span></span>

### <span data-ttu-id="fcf75-125">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="fcf75-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="fcf75-126">Note</span><span class="sxs-lookup"><span data-stu-id="fcf75-126">NOTES</span></span>

<span data-ttu-id="fcf75-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fcf75-127">ALIASES</span></span>

## <span data-ttu-id="fcf75-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcf75-128">RELATED LINKS</span></span>


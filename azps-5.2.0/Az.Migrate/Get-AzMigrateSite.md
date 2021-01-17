---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356814"
---
# <span data-ttu-id="eeade-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="eeade-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="eeade-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eeade-102">SYNOPSIS</span></span>
<span data-ttu-id="eeade-103">Metodo per ottenere un sito.</span><span class="sxs-lookup"><span data-stu-id="eeade-103">Method to get a site.</span></span>

## <span data-ttu-id="eeade-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeade-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eeade-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeade-105">DESCRIPTION</span></span>
<span data-ttu-id="eeade-106">Metodo per ottenere un sito.</span><span class="sxs-lookup"><span data-stu-id="eeade-106">Method to get a site.</span></span>

## <span data-ttu-id="eeade-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeade-107">EXAMPLES</span></span>

### <span data-ttu-id="eeade-108">Esempio 1: Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eeade-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="eeade-109">Ottenere il sito per nome</span><span class="sxs-lookup"><span data-stu-id="eeade-109">Get site by name</span></span>

## <span data-ttu-id="eeade-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eeade-110">PARAMETERS</span></span>

### <span data-ttu-id="eeade-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeade-111">-DefaultProfile</span></span>
<span data-ttu-id="eeade-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eeade-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeade-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeade-113">-Name</span></span>
<span data-ttu-id="eeade-114">Nome sito.</span><span class="sxs-lookup"><span data-stu-id="eeade-114">Site name.</span></span>

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

### <span data-ttu-id="eeade-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeade-115">-ResourceGroupName</span></span>
<span data-ttu-id="eeade-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eeade-116">The name of the resource group.</span></span>
<span data-ttu-id="eeade-117">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="eeade-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="eeade-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eeade-118">-SubscriptionId</span></span>
<span data-ttu-id="eeade-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eeade-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="eeade-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeade-120">CommonParameters</span></span>
<span data-ttu-id="eeade-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeade-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeade-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeade-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeade-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eeade-123">INPUTS</span></span>

## <span data-ttu-id="eeade-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeade-124">OUTPUTS</span></span>

### <span data-ttu-id="eeade-125">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="eeade-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="eeade-126">Note</span><span class="sxs-lookup"><span data-stu-id="eeade-126">NOTES</span></span>

<span data-ttu-id="eeade-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eeade-127">ALIASES</span></span>

## <span data-ttu-id="eeade-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeade-128">RELATED LINKS</span></span>


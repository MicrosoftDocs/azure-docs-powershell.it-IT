---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189183"
---
# <span data-ttu-id="3e33a-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="3e33a-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="3e33a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e33a-102">SYNOPSIS</span></span>

<span data-ttu-id="3e33a-103">Ottiene i piani di Azure Defender per una sottoscrizione in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="3e33a-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="3e33a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e33a-104">SYNTAX</span></span>

### <span data-ttu-id="3e33a-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e33a-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e33a-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3e33a-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e33a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e33a-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e33a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e33a-108">DESCRIPTION</span></span>

<span data-ttu-id="3e33a-109">È possibile visualizzare ogni piano di Azure Defender, per ogni abbonamento, usando questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e33a-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="3e33a-110">Per informazioni dettagliate su Azure Defender e sui piani disponibili, vedere [Introduzione ad Azure Defender.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="3e33a-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="3e33a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e33a-111">EXAMPLES</span></span>

### <span data-ttu-id="3e33a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e33a-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="3e33a-113">Ottiene lo stato di ogni piano di Azure Defender per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3e33a-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="3e33a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e33a-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="3e33a-115">Recupera i dettagli sui prezzi dell'ID risorsa specifico.</span><span class="sxs-lookup"><span data-stu-id="3e33a-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="3e33a-116">Dove ResourceId è uno degli ID restituiti da `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="3e33a-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="3e33a-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3e33a-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="3e33a-118">Recupera i dettagli sui prezzi del piano di Azure Defender denominato.</span><span class="sxs-lookup"><span data-stu-id="3e33a-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="3e33a-119">Dove `name` si trova uno dei nomi restituiti da `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="3e33a-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="3e33a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e33a-120">PARAMETERS</span></span>

### <span data-ttu-id="3e33a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e33a-121">-DefaultProfile</span></span>

<span data-ttu-id="3e33a-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e33a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e33a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3e33a-123">-Name</span></span>

<span data-ttu-id="3e33a-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e33a-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e33a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e33a-125">-ResourceId</span></span>

<span data-ttu-id="3e33a-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e33a-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e33a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e33a-127">CommonParameters</span></span>

<span data-ttu-id="3e33a-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e33a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e33a-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e33a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e33a-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e33a-130">INPUTS</span></span>

### <span data-ttu-id="3e33a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3e33a-131">System.String</span></span>

## <span data-ttu-id="3e33a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e33a-132">OUTPUTS</span></span>

### <span data-ttu-id="3e33a-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="3e33a-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="3e33a-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e33a-134">NOTES</span></span>

## <span data-ttu-id="3e33a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e33a-135">RELATED LINKS</span></span>

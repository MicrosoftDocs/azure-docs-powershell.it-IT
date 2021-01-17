---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335167"
---
# <span data-ttu-id="b2c10-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b2c10-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="b2c10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2c10-102">SYNOPSIS</span></span>

<span data-ttu-id="b2c10-103">Ottiene i piani di Azure Defender per un abbonamento in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="b2c10-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="b2c10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2c10-104">SYNTAX</span></span>

### <span data-ttu-id="b2c10-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2c10-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2c10-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b2c10-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2c10-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2c10-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2c10-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2c10-108">DESCRIPTION</span></span>

<span data-ttu-id="b2c10-109">Puoi visualizzare ogni piano di Azure Defender, per abbonamento, usando questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c10-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="b2c10-110">Per informazioni dettagliate su Azure Defender e sui piani disponibili, vedere [Introduzione a Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="b2c10-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="b2c10-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2c10-111">EXAMPLES</span></span>

### <span data-ttu-id="b2c10-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2c10-112">Example 1</span></span>

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

<span data-ttu-id="b2c10-113">Ottiene lo stato di ogni piano di Azure Defender per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b2c10-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="b2c10-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b2c10-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="b2c10-115">Ottiene i dettagli sui prezzi dell'ID risorsa specifico.</span><span class="sxs-lookup"><span data-stu-id="b2c10-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="b2c10-116">Dove ResourceId è uno degli ID restituiti da `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="b2c10-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="b2c10-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b2c10-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="b2c10-118">Ottiene i dettagli sui prezzi del piano denominato Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="b2c10-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="b2c10-119">Dove `name` è uno dei nomi restituiti da `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="b2c10-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="b2c10-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2c10-120">PARAMETERS</span></span>

### <span data-ttu-id="b2c10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c10-121">-DefaultProfile</span></span>

<span data-ttu-id="b2c10-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c10-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2c10-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2c10-123">-Name</span></span>

<span data-ttu-id="b2c10-124">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2c10-124">Resource name.</span></span>

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

### <span data-ttu-id="b2c10-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2c10-125">-ResourceId</span></span>

<span data-ttu-id="b2c10-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b2c10-126">Resource ID.</span></span>

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

### <span data-ttu-id="b2c10-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c10-127">CommonParameters</span></span>

<span data-ttu-id="b2c10-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c10-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c10-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c10-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c10-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2c10-130">INPUTS</span></span>

### <span data-ttu-id="b2c10-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b2c10-131">System.String</span></span>

## <span data-ttu-id="b2c10-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2c10-132">OUTPUTS</span></span>

### <span data-ttu-id="b2c10-133">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b2c10-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="b2c10-134">Note</span><span class="sxs-lookup"><span data-stu-id="b2c10-134">NOTES</span></span>

## <span data-ttu-id="b2c10-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2c10-135">RELATED LINKS</span></span>

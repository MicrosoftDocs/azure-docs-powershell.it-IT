---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 9d95eceac8f80280dcfadfbb20424078e6f85fce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674697"
---
# <span data-ttu-id="44219-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="44219-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="44219-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44219-102">SYNOPSIS</span></span>
<span data-ttu-id="44219-103">Ottiene informazioni sugli abbonamenti alle condivisioni consumer sul lato provider.</span><span class="sxs-lookup"><span data-stu-id="44219-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="44219-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44219-104">SYNTAX</span></span>

### <span data-ttu-id="44219-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44219-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44219-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44219-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44219-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44219-107">DESCRIPTION</span></span>
<span data-ttu-id="44219-108">Il cmdlet **Get-AzDataShareProviderSubscription** ottiene le informazioni sugli abbonamenti alle condivisioni consumer sul lato provider.</span><span class="sxs-lookup"><span data-stu-id="44219-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="44219-109">Se specifichi l'ID condivisione subscrption, questo cmdlet recupera le informazioni sull'abbonamento di condivisione.</span><span class="sxs-lookup"><span data-stu-id="44219-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="44219-110">Se non si specifica l'ID della sottoscrizione di condivisione, questo cmdlet ottiene informazioni su tutti gli abbonamenti alla condivisione consumer associati alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="44219-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="44219-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44219-111">EXAMPLES</span></span>

### <span data-ttu-id="44219-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44219-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="44219-113">Questo comando fornisce informazioni sull'abbonamento alla condivisione consumer associato a Condividi AdsShare in WikiAds dell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="44219-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="44219-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44219-114">PARAMETERS</span></span>

### <span data-ttu-id="44219-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44219-115">-AccountName</span></span>
<span data-ttu-id="44219-116">Nome dell'account di Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="44219-116">Azure DataShare Account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44219-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44219-117">-DefaultProfile</span></span>
<span data-ttu-id="44219-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44219-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44219-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44219-119">-ResourceGroupName</span></span>
<span data-ttu-id="44219-120">Gruppo risorse dell'account di Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="44219-120">The resource group of the Azure DataShare Account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44219-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44219-121">-ResourceId</span></span>
<span data-ttu-id="44219-122">ID risorsa della condivisione</span><span class="sxs-lookup"><span data-stu-id="44219-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44219-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="44219-123">-ShareName</span></span>
<span data-ttu-id="44219-124">Nome di Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="44219-124">Azure DataShare name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44219-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44219-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="44219-126">ID dell'abbonamento alla condivisione consumer</span><span class="sxs-lookup"><span data-stu-id="44219-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44219-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44219-127">CommonParameters</span></span>
<span data-ttu-id="44219-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44219-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44219-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44219-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44219-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44219-130">INPUTS</span></span>

### <span data-ttu-id="44219-131">System. String</span><span class="sxs-lookup"><span data-stu-id="44219-131">System.String</span></span>

## <span data-ttu-id="44219-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44219-132">OUTPUTS</span></span>

### <span data-ttu-id="44219-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="44219-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="44219-134">Note</span><span class="sxs-lookup"><span data-stu-id="44219-134">NOTES</span></span>

## <span data-ttu-id="44219-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44219-135">RELATED LINKS</span></span>

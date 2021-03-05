---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: b28182a5593454b110b2fe4036b022a8d74c33d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012222"
---
# <span data-ttu-id="b26eb-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b26eb-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="b26eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b26eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b26eb-103">Ottiene informazioni sulle sottoscrizioni per le condivisioni consumer sul lato provider.</span><span class="sxs-lookup"><span data-stu-id="b26eb-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="b26eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b26eb-104">SYNTAX</span></span>

### <span data-ttu-id="b26eb-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b26eb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b26eb-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b26eb-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b26eb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b26eb-107">DESCRIPTION</span></span>
<span data-ttu-id="b26eb-108">Il cmdlet **Get-AzDataShareProviderSubscription** ottiene informazioni sulle sottoscrizioni per le condivisioni consumer sul lato provider.</span><span class="sxs-lookup"><span data-stu-id="b26eb-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="b26eb-109">Se si specifica l'ID sottoscrizione della condivisione, questo cmdlet ottiene informazioni sulla sottoscrizione della condivisione.</span><span class="sxs-lookup"><span data-stu-id="b26eb-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="b26eb-110">Se non si specifica l'ID della sottoscrizione di condivisione, questo cmdlet riceve informazioni su tutte le sottoscrizioni di condivisione consumer associate alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="b26eb-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="b26eb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b26eb-111">EXAMPLES</span></span>

### <span data-ttu-id="b26eb-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b26eb-112">Example 1</span></span>
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

<span data-ttu-id="b26eb-113">Questo comando fornisce informazioni sull'abbonamento alla condivisione consumer associato a Share AdsShare nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="b26eb-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="b26eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b26eb-114">PARAMETERS</span></span>

### <span data-ttu-id="b26eb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b26eb-115">-AccountName</span></span>
<span data-ttu-id="b26eb-116">Nome account Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="b26eb-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="b26eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26eb-117">-DefaultProfile</span></span>
<span data-ttu-id="b26eb-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b26eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b26eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="b26eb-120">Gruppo di risorse dell'account Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="b26eb-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="b26eb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b26eb-121">-ResourceId</span></span>
<span data-ttu-id="b26eb-122">ID risorsa della condivisione</span><span class="sxs-lookup"><span data-stu-id="b26eb-122">The resource id of the share</span></span>

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

### <span data-ttu-id="b26eb-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b26eb-123">-ShareName</span></span>
<span data-ttu-id="b26eb-124">Nome Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="b26eb-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="b26eb-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b26eb-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="b26eb-126">ID della sottoscrizione per la condivisione consumer</span><span class="sxs-lookup"><span data-stu-id="b26eb-126">The id of consumer share subscription</span></span>

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

### <span data-ttu-id="b26eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26eb-127">CommonParameters</span></span>
<span data-ttu-id="b26eb-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26eb-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b26eb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26eb-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="b26eb-130">INPUTS</span></span>

### <span data-ttu-id="b26eb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b26eb-131">System.String</span></span>

## <span data-ttu-id="b26eb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b26eb-132">OUTPUTS</span></span>

### <span data-ttu-id="b26eb-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b26eb-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="b26eb-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="b26eb-134">NOTES</span></span>

## <span data-ttu-id="b26eb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b26eb-135">RELATED LINKS</span></span>

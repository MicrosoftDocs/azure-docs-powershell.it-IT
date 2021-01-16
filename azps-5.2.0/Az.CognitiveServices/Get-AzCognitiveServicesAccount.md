---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362053"
---
# <span data-ttu-id="aa7ae-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa7ae-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="aa7ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7ae-103">Ottiene un account.</span><span class="sxs-lookup"><span data-stu-id="aa7ae-103">Gets an account.</span></span>

## <span data-ttu-id="aa7ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa7ae-104">SYNTAX</span></span>

### <span data-ttu-id="aa7ae-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa7ae-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa7ae-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa7ae-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa7ae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa7ae-107">DESCRIPTION</span></span>
<span data-ttu-id="aa7ae-108">Il cmdlet **Get-AzCognitiveServicesAccount** ottiene gli account di servizi cognitivi con provisioning nel gruppo di risorse specificato dal parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="aa7ae-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="aa7ae-109">Se non specifichi il parametro *ResourceGroupName* , questo cmdlet ottiene tutti gli account dei servizi cognitivi per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="aa7ae-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="aa7ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa7ae-110">EXAMPLES</span></span>

### <span data-ttu-id="aa7ae-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa7ae-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="aa7ae-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa7ae-112">PARAMETERS</span></span>

### <span data-ttu-id="aa7ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7ae-113">-DefaultProfile</span></span>
<span data-ttu-id="aa7ae-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aa7ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa7ae-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa7ae-115">-Name</span></span>
<span data-ttu-id="aa7ae-116">Specifica il nome dell'account dei servizi cognitivi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="aa7ae-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa7ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa7ae-118">Specifica il nome del gruppo di risorse a cui è assegnato l'account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="aa7ae-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7ae-119">CommonParameters</span></span>
<span data-ttu-id="aa7ae-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7ae-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa7ae-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7ae-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa7ae-122">INPUTS</span></span>

### <span data-ttu-id="aa7ae-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aa7ae-123">System.String</span></span>

## <span data-ttu-id="aa7ae-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa7ae-124">OUTPUTS</span></span>

### <span data-ttu-id="aa7ae-125">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa7ae-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="aa7ae-126">Note</span><span class="sxs-lookup"><span data-stu-id="aa7ae-126">NOTES</span></span>

## <span data-ttu-id="aa7ae-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa7ae-127">RELATED LINKS</span></span>

[<span data-ttu-id="aa7ae-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa7ae-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="aa7ae-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa7ae-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="aa7ae-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa7ae-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)



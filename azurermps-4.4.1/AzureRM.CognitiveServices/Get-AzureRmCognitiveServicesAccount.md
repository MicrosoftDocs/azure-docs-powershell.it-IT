---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: c4419707c9c536a21e5fdc8aa39326b02e21937c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516988"
---
# <span data-ttu-id="b0bd0-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b0bd0-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="b0bd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bd0-103">Ottiene un account.</span><span class="sxs-lookup"><span data-stu-id="b0bd0-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0bd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0bd0-104">SYNTAX</span></span>

### <span data-ttu-id="b0bd0-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0bd0-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0bd0-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0bd0-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0bd0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0bd0-107">DESCRIPTION</span></span>
<span data-ttu-id="b0bd0-108">Il cmdlet **Get-AzureRmCognitiveServicesAccount** ottiene gli account di servizi cognitivi con provisioning nel gruppo di risorse specificato dal parametro *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0bd0-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="b0bd0-109">Se non specifichi il parametro *ResoureGroupName* , questo cmdlet ottiene tutti gli account dei servizi cognitivi per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b0bd0-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="b0bd0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0bd0-110">EXAMPLES</span></span>

## <span data-ttu-id="b0bd0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0bd0-111">PARAMETERS</span></span>

### <span data-ttu-id="b0bd0-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0bd0-112">-Name</span></span>
<span data-ttu-id="b0bd0-113">Specifica il nome dell'account dei servizi cognitivi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b0bd0-113">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="b0bd0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0bd0-114">-ResourceGroupName</span></span>
<span data-ttu-id="b0bd0-115">Specifica il nome del gruppo di risorse a cui è assegnato l'account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b0bd0-115">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="b0bd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bd0-116">-DefaultProfile</span></span>
<span data-ttu-id="b0bd0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0bd0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bd0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bd0-118">CommonParameters</span></span>
<span data-ttu-id="b0bd0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0bd0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bd0-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0bd0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bd0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0bd0-121">INPUTS</span></span>

## <span data-ttu-id="b0bd0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0bd0-122">OUTPUTS</span></span>

### <span data-ttu-id="b0bd0-123">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b0bd0-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="b0bd0-124">Note</span><span class="sxs-lookup"><span data-stu-id="b0bd0-124">NOTES</span></span>

## <span data-ttu-id="b0bd0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0bd0-125">RELATED LINKS</span></span>

[<span data-ttu-id="b0bd0-126">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b0bd0-126">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b0bd0-127">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b0bd0-127">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b0bd0-128">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b0bd0-128">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)



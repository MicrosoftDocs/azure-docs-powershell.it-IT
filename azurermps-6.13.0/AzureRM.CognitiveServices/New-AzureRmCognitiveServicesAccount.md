---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513924"
---
# <span data-ttu-id="7eed6-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7eed6-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="7eed6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eed6-102">SYNOPSIS</span></span>
<span data-ttu-id="7eed6-103">Crea un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7eed6-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eed6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eed6-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eed6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eed6-105">DESCRIPTION</span></span>
<span data-ttu-id="7eed6-106">Il cmdlet **New-AzureRmCognitiveServicesAccount** crea un account di servizi cognitivi con il tipo e SKU specificati.</span><span class="sxs-lookup"><span data-stu-id="7eed6-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="7eed6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eed6-107">EXAMPLES</span></span>

### <span data-ttu-id="7eed6-108">1:</span><span class="sxs-lookup"><span data-stu-id="7eed6-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="7eed6-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eed6-109">PARAMETERS</span></span>

### <span data-ttu-id="7eed6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eed6-110">-DefaultProfile</span></span>
<span data-ttu-id="7eed6-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7eed6-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7eed6-112">-Force</span><span class="sxs-lookup"><span data-stu-id="7eed6-112">-Force</span></span>
<span data-ttu-id="7eed6-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7eed6-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7eed6-114">-Location</span></span>
<span data-ttu-id="7eed6-115">Specifica la posizione in cui creare l'account.</span><span class="sxs-lookup"><span data-stu-id="7eed6-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7eed6-116">-Name</span></span>
<span data-ttu-id="7eed6-117">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="7eed6-117">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eed6-118">-ResourceGroupName</span></span>
<span data-ttu-id="7eed6-119">Specifica il nome del gruppo di risorse a cui assegnare l'account.</span><span class="sxs-lookup"><span data-stu-id="7eed6-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="7eed6-120">Il gruppo di risorse deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="7eed6-120">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7eed6-121">-SkuName</span></span>
<span data-ttu-id="7eed6-122">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="7eed6-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="7eed6-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7eed6-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7eed6-124">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="7eed6-124">F0 (free tier)</span></span>
- <span data-ttu-id="7eed6-125">S0</span><span class="sxs-lookup"><span data-stu-id="7eed6-125">S0</span></span>
- <span data-ttu-id="7eed6-126">S1</span><span class="sxs-lookup"><span data-stu-id="7eed6-126">S1</span></span>
- <span data-ttu-id="7eed6-127">S2</span><span class="sxs-lookup"><span data-stu-id="7eed6-127">S2</span></span>
- <span data-ttu-id="7eed6-128">S3</span><span class="sxs-lookup"><span data-stu-id="7eed6-128">S3</span></span>
- <span data-ttu-id="7eed6-129">S4 per altre informazioni, vedere [API del servizio cognitivo](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="7eed6-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="7eed6-130">-Tag</span></span>
<span data-ttu-id="7eed6-131">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="7eed6-131">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-132">-Digitare</span><span class="sxs-lookup"><span data-stu-id="7eed6-132">-Type</span></span>
<span data-ttu-id="7eed6-133">Specifica il tipo di account da creare.</span><span class="sxs-lookup"><span data-stu-id="7eed6-133">Specifies the type of account to create.</span></span> <span data-ttu-id="7eed6-134">USA `Get-AzureRmCognitiveServicesAccountType` cmdlet per ottenere i valori accettabili correnti.</span><span class="sxs-lookup"><span data-stu-id="7eed6-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7eed6-135">-Confirm</span></span>
<span data-ttu-id="7eed6-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eed6-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eed6-137">-WhatIf</span></span>
<span data-ttu-id="7eed6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7eed6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eed6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7eed6-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eed6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eed6-140">CommonParameters</span></span>
<span data-ttu-id="7eed6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eed6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eed6-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eed6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eed6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eed6-143">INPUTS</span></span>

### <span data-ttu-id="7eed6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7eed6-144">System.String</span></span>

## <span data-ttu-id="7eed6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eed6-145">OUTPUTS</span></span>

### <span data-ttu-id="7eed6-146">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7eed6-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7eed6-147">Note</span><span class="sxs-lookup"><span data-stu-id="7eed6-147">NOTES</span></span>

## <span data-ttu-id="7eed6-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eed6-148">RELATED LINKS</span></span>

[<span data-ttu-id="7eed6-149">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7eed6-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7eed6-150">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7eed6-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7eed6-151">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7eed6-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)

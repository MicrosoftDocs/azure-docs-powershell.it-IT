---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685630"
---
# <span data-ttu-id="d2854-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2854-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="d2854-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2854-102">SYNOPSIS</span></span>
<span data-ttu-id="d2854-103">Crea un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d2854-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2854-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2854-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2854-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2854-105">DESCRIPTION</span></span>
<span data-ttu-id="d2854-106">Il cmdlet **New-AzureRmCognitiveServicesAccount** crea un account di servizi cognitivi con il tipo e SKU specificati.</span><span class="sxs-lookup"><span data-stu-id="d2854-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="d2854-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2854-107">EXAMPLES</span></span>

### <span data-ttu-id="d2854-108">1:</span><span class="sxs-lookup"><span data-stu-id="d2854-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="d2854-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2854-109">PARAMETERS</span></span>

### <span data-ttu-id="d2854-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2854-110">-DefaultProfile</span></span>
<span data-ttu-id="d2854-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d2854-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d2854-112">-Force</span></span>
<span data-ttu-id="d2854-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d2854-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d2854-114">-Location</span></span>
<span data-ttu-id="d2854-115">Specifica la posizione in cui creare l'account.</span><span class="sxs-lookup"><span data-stu-id="d2854-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2854-116">-Name</span></span>
<span data-ttu-id="d2854-117">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="d2854-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2854-118">-ResourceGroupName</span></span>
<span data-ttu-id="d2854-119">Specifica il nome del gruppo di risorse a cui assegnare l'account.</span><span class="sxs-lookup"><span data-stu-id="d2854-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="d2854-120">Il gruppo di risorse deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="d2854-120">The resource group must already exist.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d2854-121">-SkuName</span></span>
<span data-ttu-id="d2854-122">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="d2854-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="d2854-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2854-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2854-124">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="d2854-124">F0 (free tier)</span></span>
- <span data-ttu-id="d2854-125">S0</span><span class="sxs-lookup"><span data-stu-id="d2854-125">S0</span></span>
- <span data-ttu-id="d2854-126">S1</span><span class="sxs-lookup"><span data-stu-id="d2854-126">S1</span></span>
- <span data-ttu-id="d2854-127">S2</span><span class="sxs-lookup"><span data-stu-id="d2854-127">S2</span></span>
- <span data-ttu-id="d2854-128">S3</span><span class="sxs-lookup"><span data-stu-id="d2854-128">S3</span></span>
- <span data-ttu-id="d2854-129">S4</span><span class="sxs-lookup"><span data-stu-id="d2854-129">S4</span></span>

<span data-ttu-id="d2854-130">Per altre informazioni, Vedi [API del servizio cognitivo](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="d2854-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2854-131">-Tag</span></span>
<span data-ttu-id="d2854-132">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="d2854-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-133">-Digitare</span><span class="sxs-lookup"><span data-stu-id="d2854-133">-Type</span></span>
<span data-ttu-id="d2854-134">Specifica il tipo di account da creare.</span><span class="sxs-lookup"><span data-stu-id="d2854-134">Specifies the type of account to create.</span></span> <span data-ttu-id="d2854-135">I valori accettabili correnti per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2854-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2854-136">Bing. Autosuggestion. V7</span><span class="sxs-lookup"><span data-stu-id="d2854-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="d2854-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="d2854-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="d2854-138">Bing. search. V7</span><span class="sxs-lookup"><span data-stu-id="d2854-138">Bing.Search.v7</span></span>
- <span data-ttu-id="d2854-139">Bing. Speech</span><span class="sxs-lookup"><span data-stu-id="d2854-139">Bing.Speech</span></span>
- <span data-ttu-id="d2854-140">Bing. SpellCheck. V7</span><span class="sxs-lookup"><span data-stu-id="d2854-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="d2854-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="d2854-141">ComputerVision</span></span>
- <span data-ttu-id="d2854-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="d2854-142">ContentModerator</span></span>
- <span data-ttu-id="d2854-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="d2854-143">CustomSpeech</span></span>
- <span data-ttu-id="d2854-144">CustomVision. Prediction</span><span class="sxs-lookup"><span data-stu-id="d2854-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="d2854-145">CustomVision. formazione</span><span class="sxs-lookup"><span data-stu-id="d2854-145">CustomVision.Training</span></span>
- <span data-ttu-id="d2854-146">Emozione</span><span class="sxs-lookup"><span data-stu-id="d2854-146">Emotion</span></span>
- <span data-ttu-id="d2854-147">Faccia</span><span class="sxs-lookup"><span data-stu-id="d2854-147">Face</span></span>
- <span data-ttu-id="d2854-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="d2854-148">LUIS</span></span>
- <span data-ttu-id="d2854-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="d2854-149">QnAMaker</span></span>
- <span data-ttu-id="d2854-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="d2854-150">SpeakerRecognition</span></span>
- <span data-ttu-id="d2854-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="d2854-151">SpeechTranslation</span></span>
- <span data-ttu-id="d2854-152">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="d2854-152">TextAnalytics</span></span>
- <span data-ttu-id="d2854-153">TextTranslation</span><span class="sxs-lookup"><span data-stu-id="d2854-153">TextTranslation</span></span>
- <span data-ttu-id="d2854-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="d2854-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2854-155">-Confirm</span></span>
<span data-ttu-id="d2854-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2854-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2854-157">-WhatIf</span></span>
<span data-ttu-id="d2854-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2854-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2854-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2854-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2854-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2854-160">CommonParameters</span></span>
<span data-ttu-id="d2854-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2854-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2854-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2854-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2854-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2854-163">INPUTS</span></span>

### <span data-ttu-id="d2854-164">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d2854-164">None</span></span>
<span data-ttu-id="d2854-165">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d2854-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2854-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2854-166">OUTPUTS</span></span>

### <span data-ttu-id="d2854-167">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2854-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="d2854-168">Note</span><span class="sxs-lookup"><span data-stu-id="d2854-168">NOTES</span></span>

## <span data-ttu-id="d2854-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2854-169">RELATED LINKS</span></span>

[<span data-ttu-id="d2854-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2854-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="d2854-171">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2854-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="d2854-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d2854-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)

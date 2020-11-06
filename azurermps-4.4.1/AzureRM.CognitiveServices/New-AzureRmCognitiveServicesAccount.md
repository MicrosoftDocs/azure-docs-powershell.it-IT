---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521780"
---
# <span data-ttu-id="b50cf-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b50cf-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="b50cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b50cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b50cf-103">Crea un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b50cf-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b50cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b50cf-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b50cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b50cf-105">DESCRIPTION</span></span>
<span data-ttu-id="b50cf-106">Il cmdlet **New-AzureRmCognitiveServicesAccount** crea un account di servizi cognitivi con il tipo e SKU specificati.</span><span class="sxs-lookup"><span data-stu-id="b50cf-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="b50cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b50cf-107">EXAMPLES</span></span>

### <span data-ttu-id="b50cf-108">1:</span><span class="sxs-lookup"><span data-stu-id="b50cf-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="b50cf-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b50cf-109">PARAMETERS</span></span>

### <span data-ttu-id="b50cf-110">-Force</span><span class="sxs-lookup"><span data-stu-id="b50cf-110">-Force</span></span>
<span data-ttu-id="b50cf-111">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b50cf-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b50cf-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b50cf-112">-Location</span></span>
<span data-ttu-id="b50cf-113">Specifica la posizione in cui creare l'account.</span><span class="sxs-lookup"><span data-stu-id="b50cf-113">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="b50cf-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b50cf-114">-Name</span></span>
<span data-ttu-id="b50cf-115">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="b50cf-115">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="b50cf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b50cf-116">-ResourceGroupName</span></span>
<span data-ttu-id="b50cf-117">Specifica il nome del gruppo di risorse a cui assegnare l'account.</span><span class="sxs-lookup"><span data-stu-id="b50cf-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="b50cf-118">Il gruppo di risorse deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="b50cf-118">The resource group must already exist.</span></span>

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

### <span data-ttu-id="b50cf-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b50cf-119">-SkuName</span></span>
<span data-ttu-id="b50cf-120">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="b50cf-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="b50cf-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b50cf-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b50cf-122">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="b50cf-122">F0 (free tier)</span></span>
- <span data-ttu-id="b50cf-123">S0</span><span class="sxs-lookup"><span data-stu-id="b50cf-123">S0</span></span>
- <span data-ttu-id="b50cf-124">S1</span><span class="sxs-lookup"><span data-stu-id="b50cf-124">S1</span></span>
- <span data-ttu-id="b50cf-125">S2</span><span class="sxs-lookup"><span data-stu-id="b50cf-125">S2</span></span>
- <span data-ttu-id="b50cf-126">S3</span><span class="sxs-lookup"><span data-stu-id="b50cf-126">S3</span></span>
- <span data-ttu-id="b50cf-127">S4</span><span class="sxs-lookup"><span data-stu-id="b50cf-127">S4</span></span>

<span data-ttu-id="b50cf-128">Per altre informazioni, Vedi [API del servizio cognitivo](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="b50cf-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="b50cf-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b50cf-129">-Tag</span></span>
<span data-ttu-id="b50cf-130">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="b50cf-130">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="b50cf-131">-Digitare</span><span class="sxs-lookup"><span data-stu-id="b50cf-131">-Type</span></span>
<span data-ttu-id="b50cf-132">Specifica il tipo di account da creare. I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b50cf-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b50cf-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="b50cf-133">ComputerVision</span></span>
- <span data-ttu-id="b50cf-134">Emozione</span><span class="sxs-lookup"><span data-stu-id="b50cf-134">Emotion</span></span>
- <span data-ttu-id="b50cf-135">Faccia</span><span class="sxs-lookup"><span data-stu-id="b50cf-135">Face</span></span>
- <span data-ttu-id="b50cf-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="b50cf-136">LUIS</span></span>
- <span data-ttu-id="b50cf-137">Raccomandazioni</span><span class="sxs-lookup"><span data-stu-id="b50cf-137">Recommendations</span></span>
- <span data-ttu-id="b50cf-138">Discorso</span><span class="sxs-lookup"><span data-stu-id="b50cf-138">Speech</span></span>
- <span data-ttu-id="b50cf-139">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="b50cf-139">TextAnalytics</span></span>
- <span data-ttu-id="b50cf-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="b50cf-140">WebLM</span></span>

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

### <span data-ttu-id="b50cf-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b50cf-141">-Confirm</span></span>
<span data-ttu-id="b50cf-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b50cf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b50cf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b50cf-143">-WhatIf</span></span>
<span data-ttu-id="b50cf-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b50cf-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b50cf-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b50cf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b50cf-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50cf-146">-DefaultProfile</span></span>
<span data-ttu-id="b50cf-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b50cf-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b50cf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50cf-148">CommonParameters</span></span>
<span data-ttu-id="b50cf-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50cf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50cf-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b50cf-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50cf-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b50cf-151">INPUTS</span></span>

## <span data-ttu-id="b50cf-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b50cf-152">OUTPUTS</span></span>

### <span data-ttu-id="b50cf-153">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b50cf-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="b50cf-154">Note</span><span class="sxs-lookup"><span data-stu-id="b50cf-154">NOTES</span></span>

## <span data-ttu-id="b50cf-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b50cf-155">RELATED LINKS</span></span>

[<span data-ttu-id="b50cf-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b50cf-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b50cf-157">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b50cf-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b50cf-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b50cf-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)

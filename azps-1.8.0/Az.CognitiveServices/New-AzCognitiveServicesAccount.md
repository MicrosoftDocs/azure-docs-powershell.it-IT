---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684851"
---
# <span data-ttu-id="b4c5e-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4c5e-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="b4c5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c5e-103">Crea un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="b4c5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4c5e-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4c5e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="b4c5e-106">Il cmdlet **New-AzCognitiveServicesAccount** crea un account di servizi cognitivi con il tipo e SKU specificati.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="b4c5e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4c5e-107">EXAMPLES</span></span>

### <span data-ttu-id="b4c5e-108">1:</span><span class="sxs-lookup"><span data-stu-id="b4c5e-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="b4c5e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4c5e-109">PARAMETERS</span></span>

### <span data-ttu-id="b4c5e-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="b4c5e-110">-CustomSubdomainName</span></span>
<span data-ttu-id="b4c5e-111">Nome del sottodominio account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="b4c5e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c5e-112">-DefaultProfile</span></span>
<span data-ttu-id="b4c5e-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b4c5e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4c5e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b4c5e-114">-Force</span></span>
<span data-ttu-id="b4c5e-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4c5e-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b4c5e-116">-Location</span></span>
<span data-ttu-id="b4c5e-117">Specifica la posizione in cui creare l'account.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="b4c5e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4c5e-118">-Name</span></span>
<span data-ttu-id="b4c5e-119">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="b4c5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4c5e-121">Specifica il nome del gruppo di risorse a cui assegnare l'account.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="b4c5e-122">Il gruppo di risorse deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="b4c5e-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4c5e-123">-SkuName</span></span>
<span data-ttu-id="b4c5e-124">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="b4c5e-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4c5e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4c5e-126">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="b4c5e-126">F0 (free tier)</span></span>
- <span data-ttu-id="b4c5e-127">S0</span><span class="sxs-lookup"><span data-stu-id="b4c5e-127">S0</span></span>
- <span data-ttu-id="b4c5e-128">S1</span><span class="sxs-lookup"><span data-stu-id="b4c5e-128">S1</span></span>
- <span data-ttu-id="b4c5e-129">S2</span><span class="sxs-lookup"><span data-stu-id="b4c5e-129">S2</span></span>
- <span data-ttu-id="b4c5e-130">S3</span><span class="sxs-lookup"><span data-stu-id="b4c5e-130">S3</span></span>
- <span data-ttu-id="b4c5e-131">S4 per altre informazioni, vedere [API del servizio cognitivo](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="b4c5e-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="b4c5e-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4c5e-132">-Tag</span></span>
<span data-ttu-id="b4c5e-133">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="b4c5e-134">-Digitare</span><span class="sxs-lookup"><span data-stu-id="b4c5e-134">-Type</span></span>
<span data-ttu-id="b4c5e-135">Specifica il tipo di account da creare.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-135">Specifies the type of account to create.</span></span> <span data-ttu-id="b4c5e-136">USA `Get-AzCognitiveServicesAccountType` cmdlet per ottenere i valori accettabili correnti.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="b4c5e-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4c5e-137">-Confirm</span></span>
<span data-ttu-id="b4c5e-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4c5e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4c5e-139">-WhatIf</span></span>
<span data-ttu-id="b4c5e-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4c5e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4c5e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c5e-142">CommonParameters</span></span>
<span data-ttu-id="b4c5e-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4c5e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c5e-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4c5e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c5e-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4c5e-145">INPUTS</span></span>

### <span data-ttu-id="b4c5e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b4c5e-146">System.String</span></span>

## <span data-ttu-id="b4c5e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4c5e-147">OUTPUTS</span></span>

### <span data-ttu-id="b4c5e-148">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4c5e-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="b4c5e-149">Note</span><span class="sxs-lookup"><span data-stu-id="b4c5e-149">NOTES</span></span>

## <span data-ttu-id="b4c5e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4c5e-150">RELATED LINKS</span></span>

[<span data-ttu-id="b4c5e-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4c5e-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="b4c5e-152">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4c5e-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="b4c5e-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b4c5e-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)

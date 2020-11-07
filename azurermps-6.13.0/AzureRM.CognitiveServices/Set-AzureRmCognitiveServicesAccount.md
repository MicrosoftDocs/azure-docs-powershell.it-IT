---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686264"
---
# <span data-ttu-id="4cbc4-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cbc4-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="4cbc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbc4-103">Modifica un account.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cbc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cbc4-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cbc4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cbc4-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbc4-106">Il cmdlet **set-AzureRmCognitiveServicesAccount** modifica l'USK o i tag dell'account dei servizi cognitivi specificati.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="4cbc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cbc4-107">EXAMPLES</span></span>

### <span data-ttu-id="4cbc4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cbc4-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="4cbc4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cbc4-109">PARAMETERS</span></span>

### <span data-ttu-id="4cbc4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbc4-110">-DefaultProfile</span></span>
<span data-ttu-id="4cbc4-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4cbc4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cbc4-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4cbc4-112">-Force</span></span>
<span data-ttu-id="4cbc4-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cbc4-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cbc4-114">-Name</span></span>
<span data-ttu-id="4cbc4-115">Specifica il nome dell'account da modificare.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="4cbc4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cbc4-116">-ResourceGroupName</span></span>
<span data-ttu-id="4cbc4-117">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="4cbc4-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4cbc4-118">-SkuName</span></span>
<span data-ttu-id="4cbc4-119">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="4cbc4-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cbc4-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4cbc4-121">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="4cbc4-121">F0 (free tier)</span></span>
- <span data-ttu-id="4cbc4-122">S0</span><span class="sxs-lookup"><span data-stu-id="4cbc4-122">S0</span></span>
- <span data-ttu-id="4cbc4-123">S1</span><span class="sxs-lookup"><span data-stu-id="4cbc4-123">S1</span></span>
- <span data-ttu-id="4cbc4-124">S2</span><span class="sxs-lookup"><span data-stu-id="4cbc4-124">S2</span></span>
- <span data-ttu-id="4cbc4-125">S3</span><span class="sxs-lookup"><span data-stu-id="4cbc4-125">S3</span></span>
- <span data-ttu-id="4cbc4-126">S4</span><span class="sxs-lookup"><span data-stu-id="4cbc4-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbc4-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="4cbc4-127">-Tag</span></span>
<span data-ttu-id="4cbc4-128">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbc4-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4cbc4-129">-Confirm</span></span>
<span data-ttu-id="4cbc4-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbc4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbc4-131">-WhatIf</span></span>
<span data-ttu-id="4cbc4-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cbc4-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbc4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbc4-134">CommonParameters</span></span>
<span data-ttu-id="4cbc4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbc4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbc4-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbc4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbc4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cbc4-137">INPUTS</span></span>

### <span data-ttu-id="4cbc4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4cbc4-138">System.String</span></span>

### <span data-ttu-id="4cbc4-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="4cbc4-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="4cbc4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cbc4-140">OUTPUTS</span></span>

### <span data-ttu-id="4cbc4-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cbc4-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4cbc4-142">Note</span><span class="sxs-lookup"><span data-stu-id="4cbc4-142">NOTES</span></span>

## <span data-ttu-id="4cbc4-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cbc4-143">RELATED LINKS</span></span>

[<span data-ttu-id="4cbc4-144">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cbc4-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4cbc4-145">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cbc4-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4cbc4-146">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4cbc4-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

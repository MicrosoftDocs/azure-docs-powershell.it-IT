---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684849"
---
# <span data-ttu-id="c8015-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c8015-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="c8015-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8015-102">SYNOPSIS</span></span>
<span data-ttu-id="c8015-103">Modifica un account.</span><span class="sxs-lookup"><span data-stu-id="c8015-103">Modifies an account.</span></span>

## <span data-ttu-id="c8015-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8015-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8015-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8015-105">DESCRIPTION</span></span>
<span data-ttu-id="c8015-106">Il cmdlet **set-AzCognitiveServicesAccount** modifica l'USK o i tag dell'account dei servizi cognitivi specificati.</span><span class="sxs-lookup"><span data-stu-id="c8015-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="c8015-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8015-107">EXAMPLES</span></span>

### <span data-ttu-id="c8015-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8015-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="c8015-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8015-109">PARAMETERS</span></span>

### <span data-ttu-id="c8015-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8015-110">-DefaultProfile</span></span>
<span data-ttu-id="c8015-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c8015-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8015-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c8015-112">-Force</span></span>
<span data-ttu-id="c8015-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c8015-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8015-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8015-114">-Name</span></span>
<span data-ttu-id="c8015-115">Specifica il nome dell'account da modificare.</span><span class="sxs-lookup"><span data-stu-id="c8015-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="c8015-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8015-116">-ResourceGroupName</span></span>
<span data-ttu-id="c8015-117">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="c8015-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="c8015-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c8015-118">-SkuName</span></span>
<span data-ttu-id="c8015-119">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="c8015-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="c8015-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8015-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8015-121">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="c8015-121">F0 (free tier)</span></span>
- <span data-ttu-id="c8015-122">S0</span><span class="sxs-lookup"><span data-stu-id="c8015-122">S0</span></span>
- <span data-ttu-id="c8015-123">S1</span><span class="sxs-lookup"><span data-stu-id="c8015-123">S1</span></span>
- <span data-ttu-id="c8015-124">S2</span><span class="sxs-lookup"><span data-stu-id="c8015-124">S2</span></span>
- <span data-ttu-id="c8015-125">S3</span><span class="sxs-lookup"><span data-stu-id="c8015-125">S3</span></span>
- <span data-ttu-id="c8015-126">S4</span><span class="sxs-lookup"><span data-stu-id="c8015-126">S4</span></span>

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

### <span data-ttu-id="c8015-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8015-127">-Tag</span></span>
<span data-ttu-id="c8015-128">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="c8015-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="c8015-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8015-129">-Confirm</span></span>
<span data-ttu-id="c8015-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8015-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8015-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8015-131">-WhatIf</span></span>
<span data-ttu-id="c8015-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8015-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8015-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8015-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8015-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8015-134">CommonParameters</span></span>
<span data-ttu-id="c8015-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8015-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8015-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8015-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8015-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8015-137">INPUTS</span></span>

### <span data-ttu-id="c8015-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c8015-138">System.String</span></span>

### <span data-ttu-id="c8015-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="c8015-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="c8015-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8015-140">OUTPUTS</span></span>

### <span data-ttu-id="c8015-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c8015-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="c8015-142">Note</span><span class="sxs-lookup"><span data-stu-id="c8015-142">NOTES</span></span>

## <span data-ttu-id="c8015-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8015-143">RELATED LINKS</span></span>

[<span data-ttu-id="c8015-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c8015-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c8015-145">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c8015-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c8015-146">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c8015-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

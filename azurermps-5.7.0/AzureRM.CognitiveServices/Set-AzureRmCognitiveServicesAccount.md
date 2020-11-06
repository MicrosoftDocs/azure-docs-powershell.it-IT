---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521094"
---
# <span data-ttu-id="7df5b-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7df5b-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="7df5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7df5b-102">SYNOPSIS</span></span>
<span data-ttu-id="7df5b-103">Modifica un account.</span><span class="sxs-lookup"><span data-stu-id="7df5b-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7df5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7df5b-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7df5b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7df5b-105">DESCRIPTION</span></span>
<span data-ttu-id="7df5b-106">Il cmdlet **set-AzureRmCognitiveServicesAccount** modifica l'USK o i tag dell'account dei servizi cognitivi specificati.</span><span class="sxs-lookup"><span data-stu-id="7df5b-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="7df5b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7df5b-107">EXAMPLES</span></span>

## <span data-ttu-id="7df5b-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7df5b-108">PARAMETERS</span></span>

### <span data-ttu-id="7df5b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df5b-109">-DefaultProfile</span></span>
<span data-ttu-id="7df5b-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7df5b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7df5b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7df5b-111">-Force</span></span>
<span data-ttu-id="7df5b-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7df5b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7df5b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7df5b-113">-Name</span></span>
<span data-ttu-id="7df5b-114">Specifica il nome dell'account da modificare.</span><span class="sxs-lookup"><span data-stu-id="7df5b-114">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="7df5b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df5b-115">-ResourceGroupName</span></span>
<span data-ttu-id="7df5b-116">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="7df5b-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="7df5b-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7df5b-117">-SkuName</span></span>
<span data-ttu-id="7df5b-118">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="7df5b-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="7df5b-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7df5b-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7df5b-120">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="7df5b-120">F0 (free tier)</span></span>
- <span data-ttu-id="7df5b-121">S0</span><span class="sxs-lookup"><span data-stu-id="7df5b-121">S0</span></span>
- <span data-ttu-id="7df5b-122">S1</span><span class="sxs-lookup"><span data-stu-id="7df5b-122">S1</span></span>
- <span data-ttu-id="7df5b-123">S2</span><span class="sxs-lookup"><span data-stu-id="7df5b-123">S2</span></span>
- <span data-ttu-id="7df5b-124">S3</span><span class="sxs-lookup"><span data-stu-id="7df5b-124">S3</span></span>
- <span data-ttu-id="7df5b-125">S4</span><span class="sxs-lookup"><span data-stu-id="7df5b-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df5b-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="7df5b-126">-Tag</span></span>
<span data-ttu-id="7df5b-127">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="7df5b-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df5b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7df5b-128">-Confirm</span></span>
<span data-ttu-id="7df5b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df5b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df5b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df5b-130">-WhatIf</span></span>
<span data-ttu-id="7df5b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7df5b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df5b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7df5b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df5b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df5b-133">CommonParameters</span></span>
<span data-ttu-id="7df5b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df5b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df5b-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df5b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df5b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7df5b-136">INPUTS</span></span>

### <span data-ttu-id="7df5b-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7df5b-137">None</span></span>
<span data-ttu-id="7df5b-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7df5b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7df5b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7df5b-139">OUTPUTS</span></span>

### <span data-ttu-id="7df5b-140">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7df5b-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7df5b-141">Note</span><span class="sxs-lookup"><span data-stu-id="7df5b-141">NOTES</span></span>

## <span data-ttu-id="7df5b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7df5b-142">RELATED LINKS</span></span>

[<span data-ttu-id="7df5b-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7df5b-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7df5b-144">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7df5b-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7df5b-145">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7df5b-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

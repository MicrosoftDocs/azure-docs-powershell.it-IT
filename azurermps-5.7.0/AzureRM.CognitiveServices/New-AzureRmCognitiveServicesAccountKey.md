---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510031"
---
# <span data-ttu-id="1294d-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="1294d-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="1294d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1294d-102">SYNOPSIS</span></span>
<span data-ttu-id="1294d-103">Rigenera una chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="1294d-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1294d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1294d-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1294d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1294d-105">DESCRIPTION</span></span>
<span data-ttu-id="1294d-106">Il cmdlet **New-AzureRmCognitiveServicesAccountKey** rigenera una chiave API per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="1294d-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="1294d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1294d-107">EXAMPLES</span></span>

## <span data-ttu-id="1294d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1294d-108">PARAMETERS</span></span>

### <span data-ttu-id="1294d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1294d-109">-DefaultProfile</span></span>
<span data-ttu-id="1294d-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1294d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1294d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1294d-111">-Force</span></span>
<span data-ttu-id="1294d-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1294d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1294d-113">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="1294d-113">-KeyName</span></span>
<span data-ttu-id="1294d-114">Specifica il nome della chiave da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="1294d-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="1294d-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1294d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1294d-116">Key1</span><span class="sxs-lookup"><span data-stu-id="1294d-116">Key1</span></span>
- <span data-ttu-id="1294d-117">Key2</span><span class="sxs-lookup"><span data-stu-id="1294d-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1294d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1294d-118">-Name</span></span>
<span data-ttu-id="1294d-119">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="1294d-119">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="1294d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1294d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1294d-121">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="1294d-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="1294d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1294d-122">-Confirm</span></span>
<span data-ttu-id="1294d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1294d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1294d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1294d-124">-WhatIf</span></span>
<span data-ttu-id="1294d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1294d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1294d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1294d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1294d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1294d-127">CommonParameters</span></span>
<span data-ttu-id="1294d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1294d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1294d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1294d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1294d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1294d-130">INPUTS</span></span>

### <span data-ttu-id="1294d-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1294d-131">None</span></span>
<span data-ttu-id="1294d-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1294d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1294d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1294d-133">OUTPUTS</span></span>

### <span data-ttu-id="1294d-134">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1294d-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="1294d-135">Note</span><span class="sxs-lookup"><span data-stu-id="1294d-135">NOTES</span></span>

## <span data-ttu-id="1294d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1294d-136">RELATED LINKS</span></span>

[<span data-ttu-id="1294d-137">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="1294d-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)



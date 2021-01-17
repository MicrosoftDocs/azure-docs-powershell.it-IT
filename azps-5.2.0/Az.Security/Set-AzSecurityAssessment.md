---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335428"
---
# <span data-ttu-id="183eb-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="183eb-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="183eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="183eb-102">SYNOPSIS</span></span>
<span data-ttu-id="183eb-103">Creare o aggiornare un risultato della valutazione della sicurezza in una risorsa</span><span class="sxs-lookup"><span data-stu-id="183eb-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="183eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="183eb-104">SYNTAX</span></span>

### <span data-ttu-id="183eb-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="183eb-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="183eb-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="183eb-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="183eb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="183eb-107">DESCRIPTION</span></span>
<span data-ttu-id="183eb-108">Creare o aggiornare un risultato della valutazione della sicurezza in una risorsa, può essere usato per cambiare lo stato di un risultato esistente o aggiungere altri dati.</span><span class="sxs-lookup"><span data-stu-id="183eb-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="183eb-109">può essere usato solo per i tipi di valutazione "CustomerManaged" e solo dopo la creazione dei metadati di valutazione corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="183eb-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="183eb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="183eb-110">EXAMPLES</span></span>

### <span data-ttu-id="183eb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="183eb-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="183eb-112">Contrassegna il risultato della sottoscrizione come "non sano" per la valutazione di tipo "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D"-altre informazioni sul tipo di valutazione verranno trovate sotto il tipo assessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="183eb-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="183eb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="183eb-113">PARAMETERS</span></span>

### <span data-ttu-id="183eb-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="183eb-114">-AdditionalData</span></span>
<span data-ttu-id="183eb-115">Dati allegati al risultato della valutazione per migliorare le indagini o la chiarezza dello stato.</span><span class="sxs-lookup"><span data-stu-id="183eb-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="183eb-116">-AssessedResourceId</span></span>
<span data-ttu-id="183eb-117">ID risorsa completa della risorsa a cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="183eb-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183eb-118">-DefaultProfile</span></span>
<span data-ttu-id="183eb-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="183eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="183eb-120">-Name</span></span>
<span data-ttu-id="183eb-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="183eb-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="183eb-122">-StatusCause</span></span>
<span data-ttu-id="183eb-123">Codice Progremmatic per la causa del risultato della valutazione.</span><span class="sxs-lookup"><span data-stu-id="183eb-123">Progremmatic code for the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="183eb-124">-StatusCode</span></span>
<span data-ttu-id="183eb-125">Codice Progremmatic per il risultato della valutazione.</span><span class="sxs-lookup"><span data-stu-id="183eb-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="183eb-126">può essere "sano", "non integro" o "NotApplicable"</span><span class="sxs-lookup"><span data-stu-id="183eb-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="183eb-127">-StatusDescription</span></span>
<span data-ttu-id="183eb-128">Descrizione leggibile umana della causa del risultato della valutazione.</span><span class="sxs-lookup"><span data-stu-id="183eb-128">Human readable description of the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="183eb-129">-Confirm</span></span>
<span data-ttu-id="183eb-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="183eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="183eb-131">-WhatIf</span></span>
<span data-ttu-id="183eb-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="183eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="183eb-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="183eb-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183eb-134">CommonParameters</span></span>
<span data-ttu-id="183eb-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="183eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183eb-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="183eb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183eb-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="183eb-137">INPUTS</span></span>

### <span data-ttu-id="183eb-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="183eb-138">None</span></span>

## <span data-ttu-id="183eb-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="183eb-139">OUTPUTS</span></span>

### <span data-ttu-id="183eb-140">Microsoft. Azure. Commands. Security. Models. assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="183eb-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="183eb-141">Note</span><span class="sxs-lookup"><span data-stu-id="183eb-141">NOTES</span></span>

## <span data-ttu-id="183eb-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="183eb-142">RELATED LINKS</span></span>

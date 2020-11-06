---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: fd07ab55fad93fdf48df52e15db846630ba6c1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521032"
---
# <span data-ttu-id="934ff-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="934ff-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="934ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="934ff-102">SYNOPSIS</span></span>
<span data-ttu-id="934ff-103">Esporta l'oggetto definizione di servizio Web come stringa formattata JSON.</span><span class="sxs-lookup"><span data-stu-id="934ff-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="934ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="934ff-104">SYNTAX</span></span>

### <span data-ttu-id="934ff-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="934ff-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="934ff-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="934ff-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="934ff-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="934ff-107">DESCRIPTION</span></span>
<span data-ttu-id="934ff-108">Esporta l'oggetto Definition per il Web serving specificato come stringa formattata JSON.</span><span class="sxs-lookup"><span data-stu-id="934ff-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="934ff-109">Puoi restituire immediatamente la stringa o salvarla in un file.</span><span class="sxs-lookup"><span data-stu-id="934ff-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="934ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="934ff-110">EXAMPLES</span></span>

### <span data-ttu-id="934ff-111">--------------------------Esempio 1: esportare come stringa--------------------------</span><span class="sxs-lookup"><span data-stu-id="934ff-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="934ff-112">--------------------------Esempio 2: esportare in un file--------------------------</span><span class="sxs-lookup"><span data-stu-id="934ff-112">--------------------------  Example 2: Export to file  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="934ff-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="934ff-113">PARAMETERS</span></span>

### <span data-ttu-id="934ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934ff-114">-DefaultProfile</span></span>
<span data-ttu-id="934ff-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="934ff-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="934ff-116">-Force</span><span class="sxs-lookup"><span data-stu-id="934ff-116">-Force</span></span>
<span data-ttu-id="934ff-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="934ff-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="934ff-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="934ff-118">-OutputFile</span></span>
<span data-ttu-id="934ff-119">Percorso del file per la definizione esportata.</span><span class="sxs-lookup"><span data-stu-id="934ff-119">The file path for exported definition.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="934ff-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="934ff-120">-ToJsonString</span></span>
<span data-ttu-id="934ff-121">Specifica che la definizione verrà esportata come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="934ff-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToJSON
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="934ff-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="934ff-122">-WebService</span></span>
<span data-ttu-id="934ff-123">Oggetto definizione del servizio Web da esportare.</span><span class="sxs-lookup"><span data-stu-id="934ff-123">The web service definition object to be exported.</span></span>

```yaml
Type: WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="934ff-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="934ff-124">-Confirm</span></span>
<span data-ttu-id="934ff-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="934ff-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="934ff-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="934ff-126">-WhatIf</span></span>
<span data-ttu-id="934ff-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="934ff-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="934ff-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="934ff-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="934ff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934ff-129">CommonParameters</span></span>
<span data-ttu-id="934ff-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="934ff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934ff-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="934ff-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934ff-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="934ff-132">INPUTS</span></span>

### <span data-ttu-id="934ff-133">Servizio</span><span class="sxs-lookup"><span data-stu-id="934ff-133">WebService</span></span>
<span data-ttu-id="934ff-134">Il parametro "WebService" accetta il valore di tipo "WebService" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="934ff-134">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="934ff-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="934ff-135">OUTPUTS</span></span>

### <span data-ttu-id="934ff-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="934ff-136">None</span></span>

## <span data-ttu-id="934ff-137">Note</span><span class="sxs-lookup"><span data-stu-id="934ff-137">NOTES</span></span>
<span data-ttu-id="934ff-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="934ff-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="934ff-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="934ff-139">RELATED LINKS</span></span>


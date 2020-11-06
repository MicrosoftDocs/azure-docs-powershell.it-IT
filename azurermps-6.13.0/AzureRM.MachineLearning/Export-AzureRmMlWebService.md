---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: 45e0fe4583477b05d4218f9e7b3ffb920b0218d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516543"
---
# <span data-ttu-id="fd253-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="fd253-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="fd253-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd253-102">SYNOPSIS</span></span>
<span data-ttu-id="fd253-103">Esporta l'oggetto definizione di servizio Web come stringa formattata JSON.</span><span class="sxs-lookup"><span data-stu-id="fd253-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd253-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd253-104">SYNTAX</span></span>

### <span data-ttu-id="fd253-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="fd253-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd253-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="fd253-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd253-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd253-107">DESCRIPTION</span></span>
<span data-ttu-id="fd253-108">Esporta l'oggetto Definition per il Web serving specificato come stringa formattata JSON.</span><span class="sxs-lookup"><span data-stu-id="fd253-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="fd253-109">Puoi restituire immediatamente la stringa o salvarla in un file.</span><span class="sxs-lookup"><span data-stu-id="fd253-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="fd253-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd253-110">EXAMPLES</span></span>

### <span data-ttu-id="fd253-111">Esempio 1: esportare come stringa</span><span class="sxs-lookup"><span data-stu-id="fd253-111">Example 1: Export as string</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="fd253-112">Esempio 2: esportare in un file</span><span class="sxs-lookup"><span data-stu-id="fd253-112">Example 2: Export to file</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="fd253-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd253-113">PARAMETERS</span></span>

### <span data-ttu-id="fd253-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd253-114">-DefaultProfile</span></span>
<span data-ttu-id="fd253-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fd253-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd253-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fd253-116">-Force</span></span>
<span data-ttu-id="fd253-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="fd253-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fd253-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="fd253-118">-OutputFile</span></span>
<span data-ttu-id="fd253-119">Percorso del file per la definizione esportata.</span><span class="sxs-lookup"><span data-stu-id="fd253-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd253-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="fd253-120">-ToJsonString</span></span>
<span data-ttu-id="fd253-121">Specifica che la definizione verrà esportata come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="fd253-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd253-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="fd253-122">-WebService</span></span>
<span data-ttu-id="fd253-123">Oggetto definizione del servizio Web da esportare.</span><span class="sxs-lookup"><span data-stu-id="fd253-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd253-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd253-124">-Confirm</span></span>
<span data-ttu-id="fd253-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd253-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd253-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd253-126">-WhatIf</span></span>
<span data-ttu-id="fd253-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd253-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd253-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd253-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd253-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd253-129">CommonParameters</span></span>
<span data-ttu-id="fd253-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd253-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd253-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd253-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd253-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd253-132">INPUTS</span></span>

### <span data-ttu-id="fd253-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="fd253-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="fd253-134">Parametri: WebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd253-134">Parameters: WebService (ByValue)</span></span>

## <span data-ttu-id="fd253-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd253-135">OUTPUTS</span></span>

### <span data-ttu-id="fd253-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fd253-136">System.String</span></span>

## <span data-ttu-id="fd253-137">Note</span><span class="sxs-lookup"><span data-stu-id="fd253-137">NOTES</span></span>
<span data-ttu-id="fd253-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fd253-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fd253-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd253-139">RELATED LINKS</span></span>

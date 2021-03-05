---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 0fad6a81f895643f8783ca8d179d68e31eed6da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976797"
---
# <span data-ttu-id="500b7-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="500b7-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="500b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500b7-102">SYNOPSIS</span></span>
<span data-ttu-id="500b7-103">Esporta l'oggetto definizione del servizio Web come stringa in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="500b7-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="500b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="500b7-104">SYNTAX</span></span>

### <span data-ttu-id="500b7-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="500b7-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500b7-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="500b7-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500b7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="500b7-107">DESCRIPTION</span></span>
<span data-ttu-id="500b7-108">Esporta l'oggetto definizione per il servizio Web specificato come stringa in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="500b7-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="500b7-109">È possibile restituire la stringa immediatamente o salvarla in un file.</span><span class="sxs-lookup"><span data-stu-id="500b7-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="500b7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="500b7-110">EXAMPLES</span></span>

### <span data-ttu-id="500b7-111">Esempio 1: Esportare come stringa</span><span class="sxs-lookup"><span data-stu-id="500b7-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="500b7-112">Esempio 2: Esportare in un file</span><span class="sxs-lookup"><span data-stu-id="500b7-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="500b7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="500b7-113">PARAMETERS</span></span>

### <span data-ttu-id="500b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500b7-114">-DefaultProfile</span></span>
<span data-ttu-id="500b7-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="500b7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="500b7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="500b7-116">-Force</span></span>
<span data-ttu-id="500b7-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="500b7-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="500b7-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="500b7-118">-OutputFile</span></span>
<span data-ttu-id="500b7-119">Percorso file per la definizione esportata.</span><span class="sxs-lookup"><span data-stu-id="500b7-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="500b7-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="500b7-120">-ToJsonString</span></span>
<span data-ttu-id="500b7-121">Specifica che la definizione verrà esportata come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="500b7-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="500b7-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="500b7-122">-WebService</span></span>
<span data-ttu-id="500b7-123">Oggetto definizione del servizio Web da esportare.</span><span class="sxs-lookup"><span data-stu-id="500b7-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="500b7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="500b7-124">-Confirm</span></span>
<span data-ttu-id="500b7-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="500b7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500b7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500b7-126">-WhatIf</span></span>
<span data-ttu-id="500b7-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="500b7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500b7-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="500b7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500b7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500b7-129">CommonParameters</span></span>
<span data-ttu-id="500b7-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500b7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500b7-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500b7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500b7-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="500b7-132">INPUTS</span></span>

### <span data-ttu-id="500b7-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="500b7-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="500b7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="500b7-134">OUTPUTS</span></span>

### <span data-ttu-id="500b7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="500b7-135">System.String</span></span>

## <span data-ttu-id="500b7-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="500b7-136">NOTES</span></span>
<span data-ttu-id="500b7-137">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="500b7-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="500b7-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="500b7-138">RELATED LINKS</span></span>

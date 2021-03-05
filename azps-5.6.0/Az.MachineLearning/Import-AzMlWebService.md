---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: e30ecc151da5e4a202b8da63f8d57a8f25c387dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961870"
---
# <span data-ttu-id="54b33-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="54b33-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="54b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54b33-102">SYNOPSIS</span></span>
<span data-ttu-id="54b33-103">Importa un oggetto JSON in una definizione di servizio Web.</span><span class="sxs-lookup"><span data-stu-id="54b33-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="54b33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54b33-104">SYNTAX</span></span>

### <span data-ttu-id="54b33-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="54b33-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54b33-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="54b33-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54b33-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="54b33-107">DESCRIPTION</span></span>
<span data-ttu-id="54b33-108">Il cmdlet Import-AzMlWebService importa, specificato direttamente o in un file a cui si fa riferimento, e crea un oggetto definizione del servizio Web che può essere passato al cmdlet New-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="54b33-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="54b33-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54b33-109">EXAMPLES</span></span>

### <span data-ttu-id="54b33-110">Esempio 1: Importare dalla stringa</span><span class="sxs-lookup"><span data-stu-id="54b33-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="54b33-111">Esempio 2: Importare da un percorso di file</span><span class="sxs-lookup"><span data-stu-id="54b33-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="54b33-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54b33-112">PARAMETERS</span></span>

### <span data-ttu-id="54b33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b33-113">-DefaultProfile</span></span>
<span data-ttu-id="54b33-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="54b33-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54b33-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="54b33-115">-InputFile</span></span>
<span data-ttu-id="54b33-116">Percorso del file contenente la definizione del servizio Web da importare.</span><span class="sxs-lookup"><span data-stu-id="54b33-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b33-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="54b33-117">-JsonString</span></span>
<span data-ttu-id="54b33-118">Stringa formattata JSON contenente la definizione del servizio Web da importare.</span><span class="sxs-lookup"><span data-stu-id="54b33-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b33-119">CommonParameters</span></span>
<span data-ttu-id="54b33-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b33-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b33-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b33-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="54b33-122">INPUTS</span></span>

### <span data-ttu-id="54b33-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="54b33-123">None</span></span>

## <span data-ttu-id="54b33-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54b33-124">OUTPUTS</span></span>

### <span data-ttu-id="54b33-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="54b33-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="54b33-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="54b33-126">NOTES</span></span>
<span data-ttu-id="54b33-127">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="54b33-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="54b33-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54b33-128">RELATED LINKS</span></span>

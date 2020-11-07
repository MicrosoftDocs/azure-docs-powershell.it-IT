---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: d85767623d88c9fd7d0a00ea98e575953132d3f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688282"
---
# <span data-ttu-id="be499-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="be499-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="be499-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be499-102">SYNOPSIS</span></span>
<span data-ttu-id="be499-103">Importa un oggetto JSON in una definizione di servizio Web.</span><span class="sxs-lookup"><span data-stu-id="be499-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be499-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be499-104">SYNTAX</span></span>

### <span data-ttu-id="be499-105">Importare da file JSON.</span><span class="sxs-lookup"><span data-stu-id="be499-105">Import from JSON file.</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be499-106">Importare da una stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="be499-106">Import from JSON string.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be499-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be499-107">DESCRIPTION</span></span>
<span data-ttu-id="be499-108">Il cmdlet Import-AzureRmMlWebService importa, specificato direttamente o in un file a cui si fa riferimento, e crea un oggetto definizione di servizio Web che può essere passato al cmdlet New-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="be499-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="be499-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be499-109">EXAMPLES</span></span>

### <span data-ttu-id="be499-110">--------------------------Esempio 1: importare da una stringa--------------------------</span><span class="sxs-lookup"><span data-stu-id="be499-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
<span data-ttu-id="be499-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="be499-111">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="be499-112">--------------------------Esempio 2: importare da un percorso di file--------------------------</span><span class="sxs-lookup"><span data-stu-id="be499-112">--------------------------  Example 2: Import from file path  --------------------------</span></span>
<span data-ttu-id="be499-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="be499-113">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="be499-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be499-114">PARAMETERS</span></span>

### <span data-ttu-id="be499-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="be499-115">-InputFile</span></span>
<span data-ttu-id="be499-116">Percorso del file che contiene la definizione del servizio Web da importare.</span><span class="sxs-lookup"><span data-stu-id="be499-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be499-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="be499-117">-JsonString</span></span>
<span data-ttu-id="be499-118">Stringa formattata JSON contenente la definizione del servizio Web da importare.</span><span class="sxs-lookup"><span data-stu-id="be499-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be499-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be499-119">-DefaultProfile</span></span>
<span data-ttu-id="be499-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be499-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be499-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be499-121">CommonParameters</span></span>
<span data-ttu-id="be499-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be499-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be499-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be499-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be499-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be499-124">INPUTS</span></span>

## <span data-ttu-id="be499-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be499-125">OUTPUTS</span></span>

### <span data-ttu-id="be499-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="be499-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="be499-127">Note</span><span class="sxs-lookup"><span data-stu-id="be499-127">NOTES</span></span>
<span data-ttu-id="be499-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="be499-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="be499-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be499-129">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516816"
---
# <span data-ttu-id="18cd0-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="18cd0-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="18cd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="18cd0-103">Controlla la disponibilità di un nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="18cd0-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18cd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18cd0-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18cd0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="18cd0-106">Il cmdlet Test-AzureRmContainerRegistryNameAvailability controlla se un nome del registro di sistema contenitore è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="18cd0-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="18cd0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="18cd0-108">Esempio 1: verifica la disponibilità di un nome del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="18cd0-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="18cd0-109">Questo comando controlla la disponibilità del nome del registro di sistema \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="18cd0-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="18cd0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18cd0-110">PARAMETERS</span></span>

### <span data-ttu-id="18cd0-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="18cd0-111">-Name</span></span>
<span data-ttu-id="18cd0-112">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="18cd0-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18cd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cd0-113">-DefaultProfile</span></span>
<span data-ttu-id="18cd0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="18cd0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18cd0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cd0-115">CommonParameters</span></span>
<span data-ttu-id="18cd0-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18cd0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cd0-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18cd0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cd0-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18cd0-118">INPUTS</span></span>

### <span data-ttu-id="18cd0-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="18cd0-119">None</span></span>
<span data-ttu-id="18cd0-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="18cd0-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18cd0-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18cd0-121">OUTPUTS</span></span>

### <span data-ttu-id="18cd0-122">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="18cd0-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="18cd0-123">Note</span><span class="sxs-lookup"><span data-stu-id="18cd0-123">NOTES</span></span>

## <span data-ttu-id="18cd0-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18cd0-124">RELATED LINKS</span></span>

[<span data-ttu-id="18cd0-125">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="18cd0-125">New-AzureRmContainerRegistry</span></span>]()


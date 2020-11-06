---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: 996dfdb0c534369aed47787601f8a2883e2af788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511791"
---
# <span data-ttu-id="fcc6c-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="fcc6c-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="fcc6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcc6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc6c-103">Controlla la disponibilità di un nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcc6c-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcc6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcc6c-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc6c-106">Il cmdlet Test-AzureRmContainerRegistryNameAvailability controlla se un nome del registro di sistema contenitore è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="fcc6c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcc6c-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc6c-108">Esempio 1: verifica la disponibilità di un nome del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="fcc6c-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="fcc6c-109">Questo comando controlla la disponibilità del nome del registro di sistema \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="fcc6c-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="fcc6c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcc6c-110">PARAMETERS</span></span>

### <span data-ttu-id="fcc6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc6c-111">-DefaultProfile</span></span>
<span data-ttu-id="fcc6c-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fcc6c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcc6c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcc6c-113">-Name</span></span>
<span data-ttu-id="fcc6c-114">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcc6c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc6c-115">CommonParameters</span></span>
<span data-ttu-id="fcc6c-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc6c-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc6c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc6c-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcc6c-118">INPUTS</span></span>

### <span data-ttu-id="fcc6c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fcc6c-119">System.String</span></span>

## <span data-ttu-id="fcc6c-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcc6c-120">OUTPUTS</span></span>

### <span data-ttu-id="fcc6c-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="fcc6c-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="fcc6c-122">Note</span><span class="sxs-lookup"><span data-stu-id="fcc6c-122">NOTES</span></span>

## <span data-ttu-id="fcc6c-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcc6c-123">RELATED LINKS</span></span>

[<span data-ttu-id="fcc6c-124">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fcc6c-124">New-AzureRmContainerRegistry</span></span>]()


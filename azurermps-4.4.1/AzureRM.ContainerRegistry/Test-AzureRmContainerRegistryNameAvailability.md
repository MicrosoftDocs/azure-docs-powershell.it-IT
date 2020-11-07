---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: ad2a97895f4876c008d1740e962bb3b746e67ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688350"
---
# <span data-ttu-id="8a718-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8a718-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="8a718-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a718-102">SYNOPSIS</span></span>
<span data-ttu-id="8a718-103">Controlla la disponibilità di un nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8a718-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a718-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a718-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a718-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a718-105">DESCRIPTION</span></span>
<span data-ttu-id="8a718-106">Il cmdlet **test-AzureRmContainerRegistryNameAvailability** controlla se un nome del registro di sistema contenitore è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="8a718-106">The **Test-AzureRmContainerRegistryNameAvailability** cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="8a718-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a718-107">EXAMPLES</span></span>

### <span data-ttu-id="8a718-108">Esempio 1: verificare la disponibilità di un nome del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="8a718-108">Example 1: Check the availability of a container registry name</span></span>
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="8a718-109">Questo comando controlla la disponibilità del nome del registro di sistema del contenitore `SomeRegistryName` .</span><span class="sxs-lookup"><span data-stu-id="8a718-109">This command checks the availability of the container registry name `SomeRegistryName`.</span></span>

## <span data-ttu-id="8a718-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a718-110">PARAMETERS</span></span>

### <span data-ttu-id="8a718-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a718-111">-Name</span></span>
<span data-ttu-id="8a718-112">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8a718-112">Container Registry Name.</span></span>

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

### <span data-ttu-id="8a718-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a718-113">-DefaultProfile</span></span>
<span data-ttu-id="8a718-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a718-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a718-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a718-115">CommonParameters</span></span>
<span data-ttu-id="8a718-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a718-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a718-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a718-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a718-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a718-118">INPUTS</span></span>

## <span data-ttu-id="8a718-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a718-119">OUTPUTS</span></span>

### <span data-ttu-id="8a718-120">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="8a718-120">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="8a718-121">Note</span><span class="sxs-lookup"><span data-stu-id="8a718-121">NOTES</span></span>

## <span data-ttu-id="8a718-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a718-122">RELATED LINKS</span></span>

[<span data-ttu-id="8a718-123">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8a718-123">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)


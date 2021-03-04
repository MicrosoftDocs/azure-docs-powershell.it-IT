---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 0a0701a073101b0611f74a9443473fcd9568ca50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956334"
---
# <span data-ttu-id="37596-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="37596-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="37596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37596-102">SYNOPSIS</span></span>
<span data-ttu-id="37596-103">Controlla la disponibilità di un nome del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="37596-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="37596-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37596-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37596-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37596-105">DESCRIPTION</span></span>
<span data-ttu-id="37596-106">Il Test-AzContainerRegistryNameAvailability cmdlet controlla se un nome del Registro di sistema del contenitore è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="37596-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="37596-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37596-107">EXAMPLES</span></span>

### <span data-ttu-id="37596-108">Esempio 1: Verifica la disponibilità di un nome del Registro di sistema del contenitore</span><span class="sxs-lookup"><span data-stu-id="37596-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="37596-109">Questo comando controlla la disponibilità del nome del Registro di sistema \` del contenitore SomeRegistryName. \`</span><span class="sxs-lookup"><span data-stu-id="37596-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="37596-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37596-110">PARAMETERS</span></span>

### <span data-ttu-id="37596-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37596-111">-DefaultProfile</span></span>
<span data-ttu-id="37596-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="37596-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37596-113">-Name</span><span class="sxs-lookup"><span data-stu-id="37596-113">-Name</span></span>
<span data-ttu-id="37596-114">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="37596-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="37596-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37596-115">CommonParameters</span></span>
<span data-ttu-id="37596-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37596-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37596-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37596-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37596-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="37596-118">INPUTS</span></span>

### <span data-ttu-id="37596-119">System.String</span><span class="sxs-lookup"><span data-stu-id="37596-119">System.String</span></span>

## <span data-ttu-id="37596-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37596-120">OUTPUTS</span></span>

### <span data-ttu-id="37596-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="37596-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="37596-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="37596-122">NOTES</span></span>

## <span data-ttu-id="37596-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37596-123">RELATED LINKS</span></span>

[<span data-ttu-id="37596-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37596-124">New-AzContainerRegistry</span></span>]()


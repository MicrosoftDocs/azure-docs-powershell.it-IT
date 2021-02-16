---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199094"
---
# <span data-ttu-id="218c3-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="218c3-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="218c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="218c3-102">SYNOPSIS</span></span>
<span data-ttu-id="218c3-103">Controlla la disponibilità di un nome del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="218c3-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="218c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="218c3-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="218c3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="218c3-105">DESCRIPTION</span></span>
<span data-ttu-id="218c3-106">Il Test-AzContainerRegistryNameAvailability cmdlet controlla se un nome del Registro di sistema del contenitore è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="218c3-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="218c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="218c3-107">EXAMPLES</span></span>

### <span data-ttu-id="218c3-108">Esempio 1: Verifica la disponibilità di un nome del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="218c3-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="218c3-109">Questo comando verifica la disponibilità del nome del Registro di sistema \` del contenitore SomeRegistryName. \`</span><span class="sxs-lookup"><span data-stu-id="218c3-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="218c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="218c3-110">PARAMETERS</span></span>

### <span data-ttu-id="218c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218c3-111">-DefaultProfile</span></span>
<span data-ttu-id="218c3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="218c3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="218c3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="218c3-113">-Name</span></span>
<span data-ttu-id="218c3-114">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="218c3-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="218c3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218c3-115">CommonParameters</span></span>
<span data-ttu-id="218c3-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="218c3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218c3-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="218c3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218c3-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="218c3-118">INPUTS</span></span>

### <span data-ttu-id="218c3-119">System.String</span><span class="sxs-lookup"><span data-stu-id="218c3-119">System.String</span></span>

## <span data-ttu-id="218c3-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="218c3-120">OUTPUTS</span></span>

### <span data-ttu-id="218c3-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="218c3-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="218c3-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="218c3-122">NOTES</span></span>

## <span data-ttu-id="218c3-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="218c3-123">RELATED LINKS</span></span>

[<span data-ttu-id="218c3-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="218c3-124">New-AzContainerRegistry</span></span>]()


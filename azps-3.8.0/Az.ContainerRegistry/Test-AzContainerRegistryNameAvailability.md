---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864515"
---
# <span data-ttu-id="133d7-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="133d7-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="133d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="133d7-102">SYNOPSIS</span></span>
<span data-ttu-id="133d7-103">Controlla la disponibilità di un nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="133d7-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="133d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="133d7-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="133d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="133d7-105">DESCRIPTION</span></span>
<span data-ttu-id="133d7-106">Il cmdlet Test-AzContainerRegistryNameAvailability controlla se un nome del registro di sistema contenitore è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="133d7-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="133d7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="133d7-107">EXAMPLES</span></span>

### <span data-ttu-id="133d7-108">Esempio 1: verifica la disponibilità di un nome del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="133d7-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="133d7-109">Questo comando controlla la disponibilità del nome del registro di sistema \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="133d7-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="133d7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="133d7-110">PARAMETERS</span></span>

### <span data-ttu-id="133d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133d7-111">-DefaultProfile</span></span>
<span data-ttu-id="133d7-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="133d7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="133d7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="133d7-113">-Name</span></span>
<span data-ttu-id="133d7-114">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="133d7-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="133d7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133d7-115">CommonParameters</span></span>
<span data-ttu-id="133d7-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="133d7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133d7-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="133d7-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133d7-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="133d7-118">INPUTS</span></span>

### <span data-ttu-id="133d7-119">System. String</span><span class="sxs-lookup"><span data-stu-id="133d7-119">System.String</span></span>

## <span data-ttu-id="133d7-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="133d7-120">OUTPUTS</span></span>

### <span data-ttu-id="133d7-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="133d7-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="133d7-122">Note</span><span class="sxs-lookup"><span data-stu-id="133d7-122">NOTES</span></span>

## <span data-ttu-id="133d7-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="133d7-123">RELATED LINKS</span></span>

[<span data-ttu-id="133d7-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="133d7-124">New-AzContainerRegistry</span></span>]()


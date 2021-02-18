---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181471"
---
# <span data-ttu-id="9ee39-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="9ee39-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="9ee39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee39-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee39-103">Ottenere l'uso di un Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee39-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="9ee39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ee39-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee39-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9ee39-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee39-106">Ottenere l'uso di un Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee39-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="9ee39-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ee39-107">EXAMPLES</span></span>

### <span data-ttu-id="9ee39-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ee39-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="9ee39-109">Ottenere l'uso di un Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee39-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="9ee39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ee39-110">PARAMETERS</span></span>

### <span data-ttu-id="9ee39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee39-111">-DefaultProfile</span></span>
<span data-ttu-id="9ee39-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee39-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee39-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9ee39-113">-Name</span></span>
<span data-ttu-id="9ee39-114">Nome del Registro di sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ee39-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee39-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee39-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ee39-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ee39-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee39-117">CommonParameters</span></span>
<span data-ttu-id="9ee39-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee39-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ee39-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee39-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="9ee39-120">INPUTS</span></span>

### <span data-ttu-id="9ee39-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9ee39-121">System.String</span></span>

## <span data-ttu-id="9ee39-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ee39-122">OUTPUTS</span></span>

### <span data-ttu-id="9ee39-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="9ee39-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="9ee39-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="9ee39-124">NOTES</span></span>

## <span data-ttu-id="9ee39-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ee39-125">RELATED LINKS</span></span>

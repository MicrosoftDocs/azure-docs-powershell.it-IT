---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: dd7ba99632cfef493fe3202b2402a938b11fa807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960765"
---
# <span data-ttu-id="1ecbf-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="1ecbf-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="1ecbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ecbf-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecbf-103">Ottieni o elenca il controller Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1ecbf-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="1ecbf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ecbf-104">SYNTAX</span></span>

### <span data-ttu-id="1ecbf-105">ListDevSpacesControllerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ecbf-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ecbf-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ecbf-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecbf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1ecbf-107">DESCRIPTION</span></span>
<span data-ttu-id="1ecbf-108">Ottieni o elenca il controller Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1ecbf-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="1ecbf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ecbf-109">EXAMPLES</span></span>

### <span data-ttu-id="1ecbf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ecbf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1ecbf-111">Elencare tutti i controller di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1ecbf-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="1ecbf-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1ecbf-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1ecbf-113">Ottieni un controller DevSpaces in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1ecbf-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="1ecbf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ecbf-114">PARAMETERS</span></span>

### <span data-ttu-id="1ecbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecbf-115">-DefaultProfile</span></span>
<span data-ttu-id="1ecbf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecbf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ecbf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1ecbf-117">-Name</span></span>
<span data-ttu-id="1ecbf-118">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1ecbf-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecbf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecbf-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ecbf-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1ecbf-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecbf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecbf-121">CommonParameters</span></span>
<span data-ttu-id="1ecbf-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ecbf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecbf-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ecbf-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecbf-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="1ecbf-124">INPUTS</span></span>

### <span data-ttu-id="1ecbf-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1ecbf-125">None</span></span>

## <span data-ttu-id="1ecbf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ecbf-126">OUTPUTS</span></span>

### <span data-ttu-id="1ecbf-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="1ecbf-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1ecbf-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="1ecbf-128">NOTES</span></span>

## <span data-ttu-id="1ecbf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ecbf-129">RELATED LINKS</span></span>

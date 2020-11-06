---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513880"
---
# <span data-ttu-id="bb4a3-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="bb4a3-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="bb4a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4a3-103">Ottenere o elencare controller di Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb4a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb4a3-104">SYNTAX</span></span>

### <span data-ttu-id="bb4a3-105">ListDevSpacesControllerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb4a3-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb4a3-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb4a3-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb4a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb4a3-107">DESCRIPTION</span></span>
<span data-ttu-id="bb4a3-108">Ottenere o elencare controller di Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="bb4a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb4a3-109">EXAMPLES</span></span>

### <span data-ttu-id="bb4a3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb4a3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="bb4a3-111">Elenca tutti i controller in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="bb4a3-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bb4a3-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="bb4a3-113">Ottenere un controller DevSpaces in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="bb4a3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb4a3-114">PARAMETERS</span></span>

### <span data-ttu-id="bb4a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4a3-115">-DefaultProfile</span></span>
<span data-ttu-id="bb4a3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb4a3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb4a3-117">-Name</span></span>
<span data-ttu-id="bb4a3-118">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="bb4a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb4a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb4a3-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bb4a3-120">Resource group name</span></span>

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

### <span data-ttu-id="bb4a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4a3-121">CommonParameters</span></span>
<span data-ttu-id="bb4a3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4a3-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb4a3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4a3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb4a3-124">INPUTS</span></span>

### <span data-ttu-id="bb4a3-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bb4a3-125">None</span></span>

## <span data-ttu-id="bb4a3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb4a3-126">OUTPUTS</span></span>

### <span data-ttu-id="bb4a3-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="bb4a3-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="bb4a3-128">Note</span><span class="sxs-lookup"><span data-stu-id="bb4a3-128">NOTES</span></span>

## <span data-ttu-id="bb4a3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb4a3-129">RELATED LINKS</span></span>

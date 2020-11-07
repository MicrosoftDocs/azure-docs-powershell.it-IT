---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 7cc4c61073b0b196faca8d95bd5153abe2587ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684427"
---
# <span data-ttu-id="3bc99-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="3bc99-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="3bc99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3bc99-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc99-103">Ottenere o elencare controller di Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="3bc99-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="3bc99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bc99-104">SYNTAX</span></span>

### <span data-ttu-id="3bc99-105">ListDevSpacesControllerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3bc99-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc99-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc99-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc99-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bc99-107">DESCRIPTION</span></span>
<span data-ttu-id="3bc99-108">Ottenere o elencare controller di Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="3bc99-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="3bc99-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bc99-109">EXAMPLES</span></span>

### <span data-ttu-id="3bc99-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3bc99-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="3bc99-111">Elenca tutti i controller in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3bc99-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="3bc99-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3bc99-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="3bc99-113">Ottenere un controller DevSpaces in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3bc99-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="3bc99-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3bc99-114">PARAMETERS</span></span>

### <span data-ttu-id="3bc99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc99-115">-DefaultProfile</span></span>
<span data-ttu-id="3bc99-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc99-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3bc99-117">-Name</span></span>
<span data-ttu-id="3bc99-118">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="3bc99-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="3bc99-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc99-119">-ResourceGroupName</span></span>
<span data-ttu-id="3bc99-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3bc99-120">Resource group name</span></span>

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

### <span data-ttu-id="3bc99-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc99-121">CommonParameters</span></span>
<span data-ttu-id="3bc99-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc99-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc99-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc99-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc99-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3bc99-124">INPUTS</span></span>

### <span data-ttu-id="3bc99-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3bc99-125">None</span></span>

## <span data-ttu-id="3bc99-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bc99-126">OUTPUTS</span></span>

### <span data-ttu-id="3bc99-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="3bc99-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="3bc99-128">Note</span><span class="sxs-lookup"><span data-stu-id="3bc99-128">NOTES</span></span>

## <span data-ttu-id="3bc99-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bc99-129">RELATED LINKS</span></span>

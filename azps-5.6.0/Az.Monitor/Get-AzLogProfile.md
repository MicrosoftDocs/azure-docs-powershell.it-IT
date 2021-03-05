---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 51dd39f18874fc1888fb37277f5de0557cf3553b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980013"
---
# <span data-ttu-id="b8c5e-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="b8c5e-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="b8c5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c5e-103">Ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="b8c5e-103">Gets a log profile.</span></span>

## <span data-ttu-id="b8c5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8c5e-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c5e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b8c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c5e-106">Il cmdlet **Get-AzLogProfile** ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="b8c5e-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="b8c5e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8c5e-107">EXAMPLES</span></span>

## <span data-ttu-id="b8c5e-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8c5e-108">PARAMETERS</span></span>

### <span data-ttu-id="b8c5e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c5e-109">-DefaultProfile</span></span>
<span data-ttu-id="b8c5e-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b8c5e-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c5e-111">-Name</span><span class="sxs-lookup"><span data-stu-id="b8c5e-111">-Name</span></span>
<span data-ttu-id="b8c5e-112">Specifica il nome del profilo di log da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b8c5e-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c5e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c5e-113">CommonParameters</span></span>
<span data-ttu-id="b8c5e-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c5e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c5e-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b8c5e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c5e-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="b8c5e-116">INPUTS</span></span>

### <span data-ttu-id="b8c5e-117">System.String</span><span class="sxs-lookup"><span data-stu-id="b8c5e-117">System.String</span></span>

## <span data-ttu-id="b8c5e-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8c5e-118">OUTPUTS</span></span>

### <span data-ttu-id="b8c5e-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="b8c5e-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="b8c5e-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="b8c5e-120">NOTES</span></span>

## <span data-ttu-id="b8c5e-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8c5e-121">RELATED LINKS</span></span>

[<span data-ttu-id="b8c5e-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="b8c5e-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="b8c5e-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="b8c5e-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202058"
---
# <span data-ttu-id="90d1c-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="90d1c-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="90d1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="90d1c-103">Ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="90d1c-103">Gets a log profile.</span></span>

## <span data-ttu-id="90d1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90d1c-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90d1c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="90d1c-106">Il cmdlet **Get-AzLogProfile** ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="90d1c-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="90d1c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90d1c-107">EXAMPLES</span></span>

## <span data-ttu-id="90d1c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90d1c-108">PARAMETERS</span></span>

### <span data-ttu-id="90d1c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d1c-109">-DefaultProfile</span></span>
<span data-ttu-id="90d1c-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="90d1c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90d1c-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="90d1c-111">-Name</span></span>
<span data-ttu-id="90d1c-112">Specifica il nome del profilo del log da ottenere.</span><span class="sxs-lookup"><span data-stu-id="90d1c-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="90d1c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d1c-113">CommonParameters</span></span>
<span data-ttu-id="90d1c-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d1c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d1c-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90d1c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d1c-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90d1c-116">INPUTS</span></span>

### <span data-ttu-id="90d1c-117">System. String</span><span class="sxs-lookup"><span data-stu-id="90d1c-117">System.String</span></span>

## <span data-ttu-id="90d1c-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90d1c-118">OUTPUTS</span></span>

### <span data-ttu-id="90d1c-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="90d1c-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="90d1c-120">Note</span><span class="sxs-lookup"><span data-stu-id="90d1c-120">NOTES</span></span>

## <span data-ttu-id="90d1c-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90d1c-121">RELATED LINKS</span></span>

[<span data-ttu-id="90d1c-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="90d1c-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="90d1c-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="90d1c-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)



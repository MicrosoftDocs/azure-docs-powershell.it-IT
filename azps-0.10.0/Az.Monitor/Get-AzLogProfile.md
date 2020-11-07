---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 5d99bafdd011409eae322c60db6e596d3c77cd4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861190"
---
# <span data-ttu-id="2ad6b-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2ad6b-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="2ad6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ad6b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad6b-103">Ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="2ad6b-103">Gets a log profile.</span></span>

## <span data-ttu-id="2ad6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ad6b-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ad6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ad6b-105">DESCRIPTION</span></span>
<span data-ttu-id="2ad6b-106">Il cmdlet **Get-AzLogProfile** ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="2ad6b-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="2ad6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ad6b-107">EXAMPLES</span></span>

## <span data-ttu-id="2ad6b-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ad6b-108">PARAMETERS</span></span>

### <span data-ttu-id="2ad6b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad6b-109">-DefaultProfile</span></span>
<span data-ttu-id="2ad6b-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2ad6b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ad6b-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ad6b-111">-Name</span></span>
<span data-ttu-id="2ad6b-112">Specifica il nome del profilo del log da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2ad6b-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="2ad6b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad6b-113">CommonParameters</span></span>
<span data-ttu-id="2ad6b-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ad6b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad6b-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ad6b-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad6b-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ad6b-116">INPUTS</span></span>

### <span data-ttu-id="2ad6b-117">System. String</span><span class="sxs-lookup"><span data-stu-id="2ad6b-117">System.String</span></span>

## <span data-ttu-id="2ad6b-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ad6b-118">OUTPUTS</span></span>

### <span data-ttu-id="2ad6b-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="2ad6b-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="2ad6b-120">Note</span><span class="sxs-lookup"><span data-stu-id="2ad6b-120">NOTES</span></span>

## <span data-ttu-id="2ad6b-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ad6b-121">RELATED LINKS</span></span>

[<span data-ttu-id="2ad6b-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2ad6b-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="2ad6b-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2ad6b-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)



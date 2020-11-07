---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 29ff6159501bccd73947e25a65ec765a49b8859c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865835"
---
# <span data-ttu-id="88eea-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="88eea-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="88eea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88eea-102">SYNOPSIS</span></span>
<span data-ttu-id="88eea-103">Ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="88eea-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88eea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88eea-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88eea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88eea-105">DESCRIPTION</span></span>
<span data-ttu-id="88eea-106">Il cmdlet **Get-AzureRmLogProfile** ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="88eea-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="88eea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88eea-107">EXAMPLES</span></span>

## <span data-ttu-id="88eea-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88eea-108">PARAMETERS</span></span>

### <span data-ttu-id="88eea-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88eea-109">-DefaultProfile</span></span>
<span data-ttu-id="88eea-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88eea-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88eea-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="88eea-111">-Name</span></span>
<span data-ttu-id="88eea-112">Specifica il nome del profilo del log da ottenere.</span><span class="sxs-lookup"><span data-stu-id="88eea-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="88eea-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88eea-113">CommonParameters</span></span>
<span data-ttu-id="88eea-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88eea-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88eea-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88eea-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88eea-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88eea-116">INPUTS</span></span>

### <span data-ttu-id="88eea-117">System. String</span><span class="sxs-lookup"><span data-stu-id="88eea-117">System.String</span></span>

## <span data-ttu-id="88eea-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88eea-118">OUTPUTS</span></span>

### <span data-ttu-id="88eea-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="88eea-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="88eea-120">Note</span><span class="sxs-lookup"><span data-stu-id="88eea-120">NOTES</span></span>

## <span data-ttu-id="88eea-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88eea-121">RELATED LINKS</span></span>

[<span data-ttu-id="88eea-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="88eea-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="88eea-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="88eea-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)



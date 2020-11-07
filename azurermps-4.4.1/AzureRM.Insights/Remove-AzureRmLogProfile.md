---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: f931f0ffb38af251be3ffb213b61f7033bb59150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686831"
---
# <span data-ttu-id="c4112-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c4112-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="c4112-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4112-102">SYNOPSIS</span></span>
<span data-ttu-id="c4112-103">Rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="c4112-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4112-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4112-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4112-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4112-105">DESCRIPTION</span></span>
<span data-ttu-id="c4112-106">Il cmdlet **Remove-AzureRmLogProfile** rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="c4112-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

## <span data-ttu-id="c4112-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4112-107">EXAMPLES</span></span>

## <span data-ttu-id="c4112-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4112-108">PARAMETERS</span></span>

### <span data-ttu-id="c4112-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4112-109">-Name</span></span>
<span data-ttu-id="c4112-110">Specifica il nome del profilo del log da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c4112-110">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="c4112-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4112-111">-DefaultProfile</span></span>
<span data-ttu-id="c4112-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4112-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4112-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4112-113">-PassThru</span></span>
<span data-ttu-id="c4112-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c4112-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4112-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4112-115">CommonParameters</span></span>
<span data-ttu-id="c4112-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4112-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4112-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4112-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4112-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4112-118">INPUTS</span></span>

## <span data-ttu-id="c4112-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4112-119">OUTPUTS</span></span>

### <span data-ttu-id="c4112-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4112-120">System.Boolean</span></span>

## <span data-ttu-id="c4112-121">Note</span><span class="sxs-lookup"><span data-stu-id="c4112-121">NOTES</span></span>

## <span data-ttu-id="c4112-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4112-122">RELATED LINKS</span></span>

[<span data-ttu-id="c4112-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c4112-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="c4112-124">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c4112-124">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)



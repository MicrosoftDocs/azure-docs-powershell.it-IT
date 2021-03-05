---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 563c97ec87a758668c737465ea50642324706a9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012221"
---
# <span data-ttu-id="c877d-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="c877d-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="c877d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c877d-102">SYNOPSIS</span></span>
<span data-ttu-id="c877d-103">Ottiene informazioni sugli inviti dei consumatori.</span><span class="sxs-lookup"><span data-stu-id="c877d-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="c877d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c877d-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c877d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c877d-105">DESCRIPTION</span></span>
<span data-ttu-id="c877d-106">Il cmdlet **Get-AzDataShareReceivedInvitation** fornisce informazioni su tutti gli inviti che il consumer ha ricevuto.</span><span class="sxs-lookup"><span data-stu-id="c877d-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="c877d-107">Se si fornisce l'ID della posizione o dell'invito, questo cmdlet fornisce informazioni sull'invito in una località specifica o sull'ID invito. In caso contrario, fornisce un elenco di inviti inviati al consumatore.</span><span class="sxs-lookup"><span data-stu-id="c877d-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="c877d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c877d-108">EXAMPLES</span></span>

### <span data-ttu-id="c877d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c877d-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="c877d-110">Questo punto e virgola fornisce informazioni sugli inviti dei consumatori.</span><span class="sxs-lookup"><span data-stu-id="c877d-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="c877d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c877d-111">PARAMETERS</span></span>

### <span data-ttu-id="c877d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c877d-112">-DefaultProfile</span></span>
<span data-ttu-id="c877d-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c877d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c877d-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="c877d-114">-InvitationId</span></span>
<span data-ttu-id="c877d-115">ID invito Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="c877d-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c877d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="c877d-116">-Location</span></span>
<span data-ttu-id="c877d-117">Percorso di invito per la condivisione di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="c877d-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c877d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c877d-118">CommonParameters</span></span>
<span data-ttu-id="c877d-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c877d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c877d-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c877d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c877d-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="c877d-121">INPUTS</span></span>

### <span data-ttu-id="c877d-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c877d-122">None</span></span>

## <span data-ttu-id="c877d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c877d-123">OUTPUTS</span></span>

### <span data-ttu-id="c877d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="c877d-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="c877d-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="c877d-125">NOTES</span></span>

## <span data-ttu-id="c877d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c877d-126">RELATED LINKS</span></span>

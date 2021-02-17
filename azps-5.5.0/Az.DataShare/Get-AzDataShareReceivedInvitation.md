---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198078"
---
# <span data-ttu-id="bd8a1-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="bd8a1-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="bd8a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8a1-103">Ottiene informazioni sugli inviti dei consumatori.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="bd8a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd8a1-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd8a1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd8a1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd8a1-106">Il cmdlet **Get-AzDataShareReceivedInvitation** fornisce informazioni su tutti gli inviti che il consumer ha ricevuto.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="bd8a1-107">Se si fornisce l'ID della posizione o dell'invito, questo cmdlet fornisce informazioni sull'invito in una località specifica o sull'ID dell'invito. In caso contrario, fornisce un elenco di inviti inviati al consumatore.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="bd8a1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd8a1-108">EXAMPLES</span></span>

### <span data-ttu-id="bd8a1-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd8a1-109">Example 1</span></span>
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

<span data-ttu-id="bd8a1-110">Questo punto e virgola fornisce informazioni sugli inviti dei consumatori.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="bd8a1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd8a1-111">PARAMETERS</span></span>

### <span data-ttu-id="bd8a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8a1-112">-DefaultProfile</span></span>
<span data-ttu-id="bd8a1-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd8a1-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="bd8a1-114">-InvitationId</span></span>
<span data-ttu-id="bd8a1-115">ID invito Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="bd8a1-116">-Location</span><span class="sxs-lookup"><span data-stu-id="bd8a1-116">-Location</span></span>
<span data-ttu-id="bd8a1-117">Percorso di invito per la condivisione di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="bd8a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8a1-118">CommonParameters</span></span>
<span data-ttu-id="bd8a1-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8a1-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd8a1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8a1-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd8a1-121">INPUTS</span></span>

### <span data-ttu-id="bd8a1-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd8a1-122">None</span></span>

## <span data-ttu-id="bd8a1-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd8a1-123">OUTPUTS</span></span>

### <span data-ttu-id="bd8a1-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="bd8a1-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="bd8a1-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd8a1-125">NOTES</span></span>

## <span data-ttu-id="bd8a1-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd8a1-126">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 7191d7b1f24909676a8b854a2b7836533401f89a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674692"
---
# <span data-ttu-id="2171f-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="2171f-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="2171f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2171f-102">SYNOPSIS</span></span>
<span data-ttu-id="2171f-103">Ottiene informazioni sugli inviti dei consumatori.</span><span class="sxs-lookup"><span data-stu-id="2171f-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="2171f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2171f-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2171f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2171f-105">DESCRIPTION</span></span>
<span data-ttu-id="2171f-106">Il cmdlet **Get-AzDataShareReceivedInvitation** fornisce informazioni su tutti gli inviti che il consumer ha receieved.</span><span class="sxs-lookup"><span data-stu-id="2171f-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="2171f-107">Se si specifica la posizione o l'ID invito, questo cmdlet fornisce informazioni su invito in particolare posizione o con ID invito. In caso contrario, fornisce un elenco di inviti inviati al consumer.</span><span class="sxs-lookup"><span data-stu-id="2171f-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="2171f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2171f-108">EXAMPLES</span></span>

### <span data-ttu-id="2171f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2171f-109">Example 1</span></span>
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

<span data-ttu-id="2171f-110">Questo comma fornisce informazioni sugli inviti dei consumatori.</span><span class="sxs-lookup"><span data-stu-id="2171f-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="2171f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2171f-111">PARAMETERS</span></span>

### <span data-ttu-id="2171f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2171f-112">-DefaultProfile</span></span>
<span data-ttu-id="2171f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2171f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2171f-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="2171f-114">-InvitationId</span></span>
<span data-ttu-id="2171f-115">ID invito di Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="2171f-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="2171f-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2171f-116">-Location</span></span>
<span data-ttu-id="2171f-117">Posizione dell'invito di condivisione dati in Azure.</span><span class="sxs-lookup"><span data-stu-id="2171f-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="2171f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2171f-118">CommonParameters</span></span>
<span data-ttu-id="2171f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2171f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2171f-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2171f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2171f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2171f-121">INPUTS</span></span>

### <span data-ttu-id="2171f-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2171f-122">None</span></span>

## <span data-ttu-id="2171f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2171f-123">OUTPUTS</span></span>

### <span data-ttu-id="2171f-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2171f-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2171f-125">Note</span><span class="sxs-lookup"><span data-stu-id="2171f-125">NOTES</span></span>

## <span data-ttu-id="2171f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2171f-126">RELATED LINKS</span></span>

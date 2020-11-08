---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: e4bff18d5b77296b470dfab8f086c101afe8e423
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018920"
---
# <span data-ttu-id="ed285-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="ed285-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="ed285-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed285-102">SYNOPSIS</span></span>
<span data-ttu-id="ed285-103">Ottiene l'invito alle informazioni della condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="ed285-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="ed285-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed285-104">SYNTAX</span></span>

### <span data-ttu-id="ed285-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed285-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed285-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed285-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed285-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed285-107">DESCRIPTION</span></span>
<span data-ttu-id="ed285-108">Il cmdlet **Get-AzDataShareInvitation** ottiene le informazioni sugli inviti aggiunti nella condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="ed285-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="ed285-109">Se specifichi il nome dell'invito, questo cmdlet ottiene le informazioni sull'invito.</span><span class="sxs-lookup"><span data-stu-id="ed285-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="ed285-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti gli inviti di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="ed285-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="ed285-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed285-111">EXAMPLES</span></span>

### <span data-ttu-id="ed285-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed285-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="ed285-113">Questo comando fornisce informazioni sull'invito AdsInvitation presente in condivisione dati AdsShare.</span><span class="sxs-lookup"><span data-stu-id="ed285-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="ed285-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed285-114">PARAMETERS</span></span>

### <span data-ttu-id="ed285-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed285-115">-AccountName</span></span>
<span data-ttu-id="ed285-116">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ed285-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed285-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed285-117">-DefaultProfile</span></span>
<span data-ttu-id="ed285-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed285-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed285-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed285-119">-Name</span></span>
<span data-ttu-id="ed285-120">Nome dell'invito della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ed285-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed285-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed285-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed285-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ed285-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed285-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed285-123">-ResourceId</span></span>
<span data-ttu-id="ed285-124">ID risorsa dell'invito di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ed285-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed285-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ed285-125">-ShareName</span></span>
<span data-ttu-id="ed285-126">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ed285-126">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed285-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed285-127">CommonParameters</span></span>
<span data-ttu-id="ed285-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed285-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed285-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed285-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed285-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed285-130">INPUTS</span></span>

### <span data-ttu-id="ed285-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ed285-131">System.String</span></span>

## <span data-ttu-id="ed285-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed285-132">OUTPUTS</span></span>

### <span data-ttu-id="ed285-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ed285-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ed285-134">Note</span><span class="sxs-lookup"><span data-stu-id="ed285-134">NOTES</span></span>

## <span data-ttu-id="ed285-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed285-135">RELATED LINKS</span></span>

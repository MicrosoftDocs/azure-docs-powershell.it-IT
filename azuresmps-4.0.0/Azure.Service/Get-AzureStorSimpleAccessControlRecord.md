---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030014"
---
# <span data-ttu-id="f23bf-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f23bf-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="f23bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f23bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f23bf-103">Ottiene i record di controllo di accesso in una configurazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="f23bf-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="f23bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f23bf-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f23bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f23bf-105">DESCRIPTION</span></span>
<span data-ttu-id="f23bf-106">Il cmdlet **Get-AzureStorSimpleAccessControlRecord** ottiene i record di controllo di accesso nella configurazione del servizio di gestione di StorSimple.</span><span class="sxs-lookup"><span data-stu-id="f23bf-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="f23bf-107">Questo cmdlet consente di ottenere tutti i record o un record denominato.</span><span class="sxs-lookup"><span data-stu-id="f23bf-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="f23bf-108">I record di controllo di Access sono contenitori di parametri dell'iniziatore iSCSI.</span><span class="sxs-lookup"><span data-stu-id="f23bf-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="f23bf-109">Questi parametri specificano quali iniziatori possono accedere a un volume.</span><span class="sxs-lookup"><span data-stu-id="f23bf-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="f23bf-110">Quando un iniziatore iSCSI cerca di connettersi a un volume, l'appliance controlla i record di controllo di accesso assegnati al volume.</span><span class="sxs-lookup"><span data-stu-id="f23bf-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="f23bf-111">Se i parametri degli iniziatori iSCSI corrispondono a una delle voci di un record di controllo di Access mappato a tale volume, l'iniziatore iSCSI può connettersi.</span><span class="sxs-lookup"><span data-stu-id="f23bf-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="f23bf-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f23bf-112">EXAMPLES</span></span>

### <span data-ttu-id="f23bf-113">Esempio 1: ottenere tutti i record di controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="f23bf-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="f23bf-114">Questo comando consente di ottenere tutti i record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="f23bf-114">This command gets all access control records.</span></span>

### <span data-ttu-id="f23bf-115">Esempio 2: ottenere un record di controllo di accesso specifico</span><span class="sxs-lookup"><span data-stu-id="f23bf-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="f23bf-116">Questo comando ottiene il record di controllo di accesso denominato Acr11.</span><span class="sxs-lookup"><span data-stu-id="f23bf-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="f23bf-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f23bf-117">PARAMETERS</span></span>

### <span data-ttu-id="f23bf-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="f23bf-118">-ACRName</span></span>
<span data-ttu-id="f23bf-119">Specifica il nome di un record di controllo di Access da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f23bf-119">Specifies the name of an access control record to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f23bf-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="f23bf-120">-Profile</span></span>
<span data-ttu-id="f23bf-121">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="f23bf-121">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f23bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23bf-122">CommonParameters</span></span>
<span data-ttu-id="f23bf-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f23bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23bf-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23bf-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f23bf-125">INPUTS</span></span>

### <span data-ttu-id="f23bf-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f23bf-126">None</span></span>

## <span data-ttu-id="f23bf-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f23bf-127">OUTPUTS</span></span>

### <span data-ttu-id="f23bf-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="f23bf-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="f23bf-129">Questo cmdlet restituisce un oggetto **AccessControlRecord** o un **oggetto \<AccessControlRecord\> IList** .</span><span class="sxs-lookup"><span data-stu-id="f23bf-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="f23bf-130">Un oggetto **AccessControlRecord** contiene i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f23bf-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="f23bf-131">**GlobalId** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="f23bf-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="f23bf-132">**Initiatorname** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f23bf-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="f23bf-133">**InstanceID** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="f23bf-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="f23bf-134">**Nome** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="f23bf-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="f23bf-135">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="f23bf-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="f23bf-136">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="f23bf-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="f23bf-137">Note</span><span class="sxs-lookup"><span data-stu-id="f23bf-137">NOTES</span></span>

## <span data-ttu-id="f23bf-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f23bf-138">RELATED LINKS</span></span>

[<span data-ttu-id="f23bf-139">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f23bf-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="f23bf-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f23bf-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="f23bf-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f23bf-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)



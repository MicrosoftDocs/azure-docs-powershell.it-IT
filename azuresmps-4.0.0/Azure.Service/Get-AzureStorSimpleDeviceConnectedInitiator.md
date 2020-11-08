---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029753"
---
# <span data-ttu-id="0ca84-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="0ca84-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="0ca84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ca84-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca84-103">Ottiene le connessioni iSCSI disponibili per un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0ca84-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="0ca84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ca84-104">SYNTAX</span></span>

### <span data-ttu-id="0ca84-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="0ca84-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0ca84-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="0ca84-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ca84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ca84-107">DESCRIPTION</span></span>
<span data-ttu-id="0ca84-108">Il cmdlet **Get-AzureStorSimpleDeviceConnectedInitiator** ottiene un elenco delle connessioni iSCSI disponibili per un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0ca84-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="0ca84-109">Gli oggetti connessione iSCSI restituiti dal cmdlet contengono le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ca84-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="0ca84-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="0ca84-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="0ca84-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="0ca84-111">**AcrName**</span></span>
- <span data-ttu-id="0ca84-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="0ca84-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="0ca84-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="0ca84-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="0ca84-114">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="0ca84-114">**Interfaces**</span></span>
- <span data-ttu-id="0ca84-115">**IQN**</span><span class="sxs-lookup"><span data-stu-id="0ca84-115">**Iqn**</span></span>
- <span data-ttu-id="0ca84-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="0ca84-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="0ca84-117">Questo cmdlet ottiene l'oggetto Connection solo se le connessioni iSCSI sono attivate per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ca84-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="0ca84-118">Per impostazione predefinita, le connessioni sono disattivate.</span><span class="sxs-lookup"><span data-stu-id="0ca84-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="0ca84-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ca84-119">EXAMPLES</span></span>

### <span data-ttu-id="0ca84-120">Esempio 1: ottenere tutte le connessioni per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="0ca84-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="0ca84-121">Questo comando consente di ottenere tutte le connessioni iSCSI per il dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="0ca84-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="0ca84-122">Questo comando restituisce le connessioni solo se le connessioni sono attivate per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ca84-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="0ca84-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ca84-123">PARAMETERS</span></span>

### <span data-ttu-id="0ca84-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0ca84-124">-DeviceId</span></span>
<span data-ttu-id="0ca84-125">Specifica l'ID istanza del dispositivo StorSimple da cui ottenere gli iniziatori iSCSI.</span><span class="sxs-lookup"><span data-stu-id="0ca84-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca84-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0ca84-126">-DeviceName</span></span>
<span data-ttu-id="0ca84-127">Specifica il nome del dispositivo StorSimple da cui ottenere gli iniziatori iSCSI.</span><span class="sxs-lookup"><span data-stu-id="0ca84-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca84-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="0ca84-128">-Profile</span></span>
<span data-ttu-id="0ca84-129">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca84-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0ca84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca84-130">CommonParameters</span></span>
<span data-ttu-id="0ca84-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca84-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ca84-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca84-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ca84-133">INPUTS</span></span>

### <span data-ttu-id="0ca84-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ca84-134">None</span></span>

## <span data-ttu-id="0ca84-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ca84-135">OUTPUTS</span></span>

### <span data-ttu-id="0ca84-136">Elenco\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="0ca84-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="0ca84-137">Questo cmdlet restituisce un oggetto connessione iSCSI che contiene le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ca84-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="0ca84-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="0ca84-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="0ca84-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="0ca84-139">**AcrName**</span></span>
- <span data-ttu-id="0ca84-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="0ca84-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="0ca84-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="0ca84-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="0ca84-142">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="0ca84-142">**Interfaces**</span></span>
- <span data-ttu-id="0ca84-143">**IQN**</span><span class="sxs-lookup"><span data-stu-id="0ca84-143">**Iqn**</span></span>
- <span data-ttu-id="0ca84-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="0ca84-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="0ca84-145">Note</span><span class="sxs-lookup"><span data-stu-id="0ca84-145">NOTES</span></span>

## <span data-ttu-id="0ca84-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ca84-146">RELATED LINKS</span></span>

[<span data-ttu-id="0ca84-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="0ca84-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)



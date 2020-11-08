---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023519"
---
# <span data-ttu-id="b1cc0-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="b1cc0-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="b1cc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cc0-103">Ottiene i gruppi di contenitori del volume per il failover del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="b1cc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1cc0-104">SYNTAX</span></span>

### <span data-ttu-id="b1cc0-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="b1cc0-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b1cc0-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="b1cc0-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1cc0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1cc0-107">DESCRIPTION</span></span>
<span data-ttu-id="b1cc0-108">Il cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** ottiene i gruppi di contenitori del volume per il failover del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="b1cc0-109">Passare un singolo gruppo di **VolumeContainer** o una matrice di gruppi di **VolumeContainer** al cmdlet **Start-AzureStorSimpleDeviceFailover** .</span><span class="sxs-lookup"><span data-stu-id="b1cc0-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="b1cc0-110">Solo i gruppi che hanno un valore di $True per la proprietà **IsDCGroupEligibleForDR** sono idonei per il failover.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="b1cc0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1cc0-111">EXAMPLES</span></span>

### <span data-ttu-id="b1cc0-112">Esempio 1: ottenere i contenitori del volume di failover</span><span class="sxs-lookup"><span data-stu-id="b1cc0-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="b1cc0-113">Questo comando ottiene i contenitori del volume di failover.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="b1cc0-114">Per il failover dei dispositivi può essere usato solo il DCGroups che ha un valore di $True per la proprietà **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="b1cc0-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="b1cc0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1cc0-115">PARAMETERS</span></span>

### <span data-ttu-id="b1cc0-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b1cc0-116">-DeviceId</span></span>
<span data-ttu-id="b1cc0-117">Specifica l'ID istanza del dispositivo StorSimple in cui eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cc0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b1cc0-118">-DeviceName</span></span>
<span data-ttu-id="b1cc0-119">Specifica il nome del dispositivo StorSimple in cui eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cc0-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1cc0-120">-Profile</span></span>
<span data-ttu-id="b1cc0-121">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b1cc0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cc0-122">CommonParameters</span></span>
<span data-ttu-id="b1cc0-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1cc0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cc0-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cc0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cc0-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1cc0-125">INPUTS</span></span>

## <span data-ttu-id="b1cc0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1cc0-126">OUTPUTS</span></span>

### <span data-ttu-id="b1cc0-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="b1cc0-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="b1cc0-128">Questo cmdlet restituisce un elenco di gruppi di **VolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="b1cc0-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="b1cc0-129">Note</span><span class="sxs-lookup"><span data-stu-id="b1cc0-129">NOTES</span></span>

## <span data-ttu-id="b1cc0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1cc0-130">RELATED LINKS</span></span>

[<span data-ttu-id="b1cc0-131">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b1cc0-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="b1cc0-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b1cc0-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)



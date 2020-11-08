---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023583"
---
# <span data-ttu-id="86574-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="86574-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="86574-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86574-102">SYNOPSIS</span></span>
<span data-ttu-id="86574-103">Recupera lo script di configurazione per un dispositivo VPN di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="86574-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="86574-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86574-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86574-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86574-105">DESCRIPTION</span></span>
<span data-ttu-id="86574-106">Il cmdlet **Get-AzureRemoteAppVpnDeviceConfigScript** recupera lo script di configurazione per un dispositivo VPN (Virtual Private Network) di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="86574-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="86574-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86574-107">EXAMPLES</span></span>

### <span data-ttu-id="86574-108">Esempio 1: ottenere uno script di configurazione per un dispositivo VPN</span><span class="sxs-lookup"><span data-stu-id="86574-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="86574-109">Questo comando restituisce lo script o il file di configurazione usato per configurare il dispositivo VPN per la rete virtuale denominata ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="86574-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="86574-110">Questo file di script o configurazione deve essere eseguito o caricato sul dispositivo VPN in modo tipico per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86574-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="86574-111">Consulta il fornitore di dispositivi VPN per i requisiti univoci per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86574-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="86574-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86574-112">PARAMETERS</span></span>

### <span data-ttu-id="86574-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="86574-113">-OSFamily</span></span>
<span data-ttu-id="86574-114">Specifica la famiglia di sistemi operativi (OS) che viene eseguita nella piattaforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86574-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86574-115">-Platform</span><span class="sxs-lookup"><span data-stu-id="86574-115">-Platform</span></span>
<span data-ttu-id="86574-116">Specifica la piattaforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86574-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86574-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="86574-117">-Profile</span></span>
<span data-ttu-id="86574-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86574-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86574-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="86574-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86574-120">-Vendor</span><span class="sxs-lookup"><span data-stu-id="86574-120">-Vendor</span></span>
<span data-ttu-id="86574-121">Specifica il fornitore del dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="86574-121">Specifies the vendor of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86574-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="86574-122">-VNetName</span></span>
<span data-ttu-id="86574-123">Specifica il nome di una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="86574-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86574-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86574-124">CommonParameters</span></span>
<span data-ttu-id="86574-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86574-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86574-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86574-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86574-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86574-127">INPUTS</span></span>

## <span data-ttu-id="86574-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86574-128">OUTPUTS</span></span>

## <span data-ttu-id="86574-129">Note</span><span class="sxs-lookup"><span data-stu-id="86574-129">NOTES</span></span>

## <span data-ttu-id="86574-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86574-130">RELATED LINKS</span></span>

[<span data-ttu-id="86574-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="86574-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)



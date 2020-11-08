---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023429"
---
# <span data-ttu-id="00ab3-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="00ab3-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="00ab3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="00ab3-103">Reimposta la chiave condivisa di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="00ab3-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="00ab3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00ab3-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00ab3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="00ab3-106">Il cmdlet **Reset-AzureRemoteAppVpnSharedKey** Reimposta la chiave condivisa Virtual Private Network (VPN) di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="00ab3-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="00ab3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="00ab3-108">Esempio 1: reimpostare la chiave condivisa in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="00ab3-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="00ab3-109">Questo comando Reimposta la chiave condivisa nella rete virtuale denominata ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="00ab3-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="00ab3-110">La connessione VPN alla rete locale rimane offline finché non viene configurata la nuova chiave condivisa nel dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="00ab3-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="00ab3-111">Per configurare il dispositivo VPN, usare il cmdlet **Get-AzureRemoteAppVpnDeviceConfigScript** per recuperare lo script o il file di configurazione corretto per il dispositivo VPN, quindi caricare lo script o il file di configurazione nel dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="00ab3-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="00ab3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00ab3-112">PARAMETERS</span></span>

### <span data-ttu-id="00ab3-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="00ab3-113">-Profile</span></span>
<span data-ttu-id="00ab3-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00ab3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00ab3-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="00ab3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00ab3-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="00ab3-116">-VNetName</span></span>
<span data-ttu-id="00ab3-117">Specifica il nome della rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="00ab3-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="00ab3-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00ab3-118">-Confirm</span></span>
<span data-ttu-id="00ab3-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00ab3-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ab3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ab3-120">-WhatIf</span></span>
<span data-ttu-id="00ab3-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00ab3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00ab3-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00ab3-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ab3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ab3-123">CommonParameters</span></span>
<span data-ttu-id="00ab3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ab3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ab3-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ab3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ab3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00ab3-126">INPUTS</span></span>

## <span data-ttu-id="00ab3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00ab3-127">OUTPUTS</span></span>

### <span data-ttu-id="00ab3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00ab3-128">System.String</span></span>

## <span data-ttu-id="00ab3-129">Note</span><span class="sxs-lookup"><span data-stu-id="00ab3-129">NOTES</span></span>

## <span data-ttu-id="00ab3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00ab3-130">RELATED LINKS</span></span>

[<span data-ttu-id="00ab3-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="00ab3-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="00ab3-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="00ab3-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)



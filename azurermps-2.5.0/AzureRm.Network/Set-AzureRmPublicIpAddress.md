---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: d78e4d8e84508e9a737bb15dc31b0dad1c9bdedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866217"
---
# <span data-ttu-id="0db13-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0db13-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="0db13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0db13-102">SYNOPSIS</span></span>
<span data-ttu-id="0db13-103">Imposta lo stato obiettivo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="0db13-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0db13-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0db13-105">DESCRIPTION</span></span>
<span data-ttu-id="0db13-106">Il cmdlet **set-AzureRmPublicIpAddress** imposta lo stato dell'obiettivo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="0db13-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="0db13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0db13-107">EXAMPLES</span></span>

### <span data-ttu-id="0db13-108">1: cambiare il metodo di assegnazione di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0db13-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="0db13-109">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="0db13-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="0db13-110">Secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "static".</span><span class="sxs-lookup"><span data-stu-id="0db13-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="0db13-111">Set-AzureRmPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di allocazione in "static".</span><span class="sxs-lookup"><span data-stu-id="0db13-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="0db13-112">Viene allocato immediatamente un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="0db13-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="0db13-113">2: modificare l'etichetta del dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0db13-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="0db13-114">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="0db13-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="0db13-115">Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0db13-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="0db13-116">Set-AzureRmPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="0db13-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="0db13-117">DomainNameLabel & FQDN vengono modificati come previsto.</span><span class="sxs-lookup"><span data-stu-id="0db13-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="0db13-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0db13-118">PARAMETERS</span></span>

### <span data-ttu-id="0db13-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0db13-119">-AsJob</span></span>
<span data-ttu-id="0db13-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0db13-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db13-121">-DefaultProfile</span></span>
<span data-ttu-id="0db13-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0db13-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db13-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0db13-123">-PublicIpAddress</span></span>
<span data-ttu-id="0db13-124">Specifica un oggetto **PublicIpAddress** che rappresenta lo stato dell'obiettivo a cui deve essere impostato l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="0db13-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db13-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db13-125">CommonParameters</span></span>
<span data-ttu-id="0db13-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db13-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db13-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db13-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db13-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0db13-128">INPUTS</span></span>

### <span data-ttu-id="0db13-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0db13-129">PSPublicIpAddress</span></span>
<span data-ttu-id="0db13-130">Il parametro ' PublicIpAddress ' accetta il valore di tipo ' PSPublicIpAddress ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0db13-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="0db13-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0db13-131">OUTPUTS</span></span>

### <span data-ttu-id="0db13-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0db13-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0db13-133">Note</span><span class="sxs-lookup"><span data-stu-id="0db13-133">NOTES</span></span>

## <span data-ttu-id="0db13-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0db13-134">RELATED LINKS</span></span>

[<span data-ttu-id="0db13-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0db13-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0db13-136">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0db13-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0db13-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0db13-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)



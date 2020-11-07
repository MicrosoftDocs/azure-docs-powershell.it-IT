---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862741"
---
# <span data-ttu-id="bab6b-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bab6b-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="bab6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bab6b-102">SYNOPSIS</span></span>
<span data-ttu-id="bab6b-103">Imposta lo stato obiettivo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="bab6b-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="bab6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bab6b-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bab6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bab6b-105">DESCRIPTION</span></span>
<span data-ttu-id="bab6b-106">Il cmdlet **set-AzPublicIpAddress** imposta lo stato dell'obiettivo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="bab6b-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="bab6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bab6b-107">EXAMPLES</span></span>

### <span data-ttu-id="bab6b-108">1: cambiare il metodo di assegnazione di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="bab6b-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="bab6b-109">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="bab6b-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="bab6b-110">Secondo comando imposta il metodo di allocazione dell'oggetto indirizzo IP pubblico su "static".</span><span class="sxs-lookup"><span data-stu-id="bab6b-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="bab6b-111">Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato e modifica il metodo di allocazione in "static".</span><span class="sxs-lookup"><span data-stu-id="bab6b-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="bab6b-112">Viene allocato immediatamente un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="bab6b-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="bab6b-113">2: modificare l'etichetta del dominio DNS di un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="bab6b-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="bab6b-114">Il primo comando ottiene la risorsa indirizzo IP pubblico con il nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="bab6b-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="bab6b-115">Secondo comando imposta la proprietà DomainNameLabel sul prefisso DNS obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bab6b-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="bab6b-116">Set-AzPublicIPAddress comando Aggiorna la risorsa indirizzo IP pubblico con l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bab6b-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="bab6b-117">DomainNameLabel & FQDN vengono modificati come previsto.</span><span class="sxs-lookup"><span data-stu-id="bab6b-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="bab6b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bab6b-118">PARAMETERS</span></span>

### <span data-ttu-id="bab6b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bab6b-119">-AsJob</span></span>
<span data-ttu-id="bab6b-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bab6b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bab6b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab6b-121">-DefaultProfile</span></span>
<span data-ttu-id="bab6b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bab6b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab6b-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bab6b-123">-PublicIpAddress</span></span>
<span data-ttu-id="bab6b-124">Specifica un oggetto **PublicIpAddress** che rappresenta lo stato dell'obiettivo a cui deve essere impostato l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="bab6b-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="bab6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab6b-125">CommonParameters</span></span>
<span data-ttu-id="bab6b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab6b-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab6b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab6b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bab6b-128">INPUTS</span></span>

### <span data-ttu-id="bab6b-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bab6b-129">PSPublicIpAddress</span></span>
<span data-ttu-id="bab6b-130">Il parametro ' PublicIpAddress ' accetta il valore di tipo ' PSPublicIpAddress ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bab6b-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="bab6b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bab6b-131">OUTPUTS</span></span>

### <span data-ttu-id="bab6b-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bab6b-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="bab6b-133">Note</span><span class="sxs-lookup"><span data-stu-id="bab6b-133">NOTES</span></span>

## <span data-ttu-id="bab6b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bab6b-134">RELATED LINKS</span></span>

[<span data-ttu-id="bab6b-135">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bab6b-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="bab6b-136">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bab6b-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="bab6b-137">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bab6b-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)



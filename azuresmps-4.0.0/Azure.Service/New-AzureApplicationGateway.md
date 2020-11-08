---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029688"
---
# <span data-ttu-id="f4c82-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4c82-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="f4c82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4c82-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c82-103">Crea un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-103">Creates an application gateway.</span></span>

## <span data-ttu-id="f4c82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4c82-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4c82-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4c82-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c82-106">Il cmdlet **New-AzureApplicationGateway** crea un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="f4c82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4c82-107">EXAMPLES</span></span>

### <span data-ttu-id="f4c82-108">Esempio 1: creare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f4c82-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="f4c82-109">Questo comando crea un gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="f4c82-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="f4c82-110">Il comando distribuisce il gateway in VirtualNetwork17 e nelle subnet specificate.</span><span class="sxs-lookup"><span data-stu-id="f4c82-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="f4c82-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4c82-111">PARAMETERS</span></span>

### <span data-ttu-id="f4c82-112">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4c82-112">-Description</span></span>
<span data-ttu-id="f4c82-113">Specifica una descrizione che questo cmdlet assegna al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c82-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="f4c82-114">-GatewaySize</span></span>
<span data-ttu-id="f4c82-115">Specifica le dimensioni assegnate dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="f4c82-116">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f4c82-116">Valid values are:</span></span>

- <span data-ttu-id="f4c82-117">Small</span><span class="sxs-lookup"><span data-stu-id="f4c82-117">Small</span></span>
- <span data-ttu-id="f4c82-118">Medio</span><span class="sxs-lookup"><span data-stu-id="f4c82-118">Medium</span></span>
- <span data-ttu-id="f4c82-119">Grande</span><span class="sxs-lookup"><span data-stu-id="f4c82-119">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c82-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="f4c82-120">-InstanceCount</span></span>
<span data-ttu-id="f4c82-121">Specifica il numero di istanze assegnate dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c82-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4c82-122">-Name</span></span>
<span data-ttu-id="f4c82-123">Specifica un nome per il nuovo gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-123">Specifies a name for the new application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c82-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="f4c82-124">-Profile</span></span>
<span data-ttu-id="f4c82-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c82-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4c82-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f4c82-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4c82-127">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f4c82-127">-Subnets</span></span>
<span data-ttu-id="f4c82-128">Specifica una matrice di subnet in cui questo cmdlet distribuisce il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c82-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="f4c82-129">-VnetName</span></span>
<span data-ttu-id="f4c82-130">Specifica la rete virtuale in cui questo cmdlet distribuisce il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4c82-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c82-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c82-131">CommonParameters</span></span>
<span data-ttu-id="f4c82-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c82-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c82-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c82-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c82-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4c82-134">INPUTS</span></span>

### <span data-ttu-id="f4c82-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f4c82-135">System.String</span></span>

## <span data-ttu-id="f4c82-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4c82-136">OUTPUTS</span></span>

### <span data-ttu-id="f4c82-137">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f4c82-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="f4c82-138">Note</span><span class="sxs-lookup"><span data-stu-id="f4c82-138">NOTES</span></span>

## <span data-ttu-id="f4c82-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4c82-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4c82-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4c82-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="f4c82-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4c82-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="f4c82-142">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4c82-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="f4c82-143">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4c82-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="f4c82-144">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4c82-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)

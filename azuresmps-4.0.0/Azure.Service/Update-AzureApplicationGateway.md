---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023802"
---
# <span data-ttu-id="cf733-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf733-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="cf733-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf733-102">SYNOPSIS</span></span>
<span data-ttu-id="cf733-103">Aggiorna un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-103">Updates an application gateway.</span></span>

## <span data-ttu-id="cf733-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf733-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf733-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf733-105">DESCRIPTION</span></span>
<span data-ttu-id="cf733-106">Il cmdlet **Update-AzureApplicationGateway** aggiorna un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="cf733-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="cf733-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf733-107">EXAMPLES</span></span>

### <span data-ttu-id="cf733-108">Esempio 1: modificare un gateway dell'applicazione usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="cf733-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="cf733-109">Il primo comando Arresta il gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="cf733-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="cf733-110">Per poter modificare la rete virtuale o le subnet, è necessario arrestare un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="cf733-111">Il secondo comando consente di modificare la subnet virtuale e le subnet per il gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="cf733-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="cf733-112">Esempio 2: modificare altre proprietà di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="cf733-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="cf733-113">Questo comando modifica il conteggio delle istanze, le dimensioni del gateway e la descrizione per il gateway dell'applicazione denominato ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="cf733-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="cf733-114">Questo comando non modifica la rete virtuale o le subnet per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="cf733-115">Non è pertanto necessario arrestare il gateway dell'applicazione prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="cf733-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="cf733-116">Esempio 3: modificare un gateway dell'applicazione usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="cf733-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="cf733-117">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway06 usando il cmdlet **Get-AzureApplicationGateway** .</span><span class="sxs-lookup"><span data-stu-id="cf733-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="cf733-118">Il comando lo archivia nella variabile $ApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="cf733-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="cf733-119">Il secondo comando assegna la proprietà **GatewaySize** il valore Medium.</span><span class="sxs-lookup"><span data-stu-id="cf733-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="cf733-120">Il comando finale passa la $ApplicationGateway aggiornata al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="cf733-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="cf733-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf733-121">PARAMETERS</span></span>

### <span data-ttu-id="cf733-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf733-122">-Description</span></span>
<span data-ttu-id="cf733-123">Specifica una descrizione che questo cmdlet assegna al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="cf733-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="cf733-124">-GatewaySize</span></span>
<span data-ttu-id="cf733-125">Specifica le dimensioni assegnate dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="cf733-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="cf733-126">Valid values are:</span></span>

- <span data-ttu-id="cf733-127">Small</span><span class="sxs-lookup"><span data-stu-id="cf733-127">Small</span></span>
- <span data-ttu-id="cf733-128">Medio</span><span class="sxs-lookup"><span data-stu-id="cf733-128">Medium</span></span>
- <span data-ttu-id="cf733-129">Grande</span><span class="sxs-lookup"><span data-stu-id="cf733-129">Large</span></span>

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

### <span data-ttu-id="cf733-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="cf733-130">-InstanceCount</span></span>
<span data-ttu-id="cf733-131">Specifica il numero di istanze assegnate dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="cf733-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf733-132">-Name</span></span>
<span data-ttu-id="cf733-133">Specifica il nome del gateway dell'applicazione che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="cf733-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="cf733-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="cf733-134">-Profile</span></span>
<span data-ttu-id="cf733-135">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf733-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf733-136">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="cf733-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf733-137">-Subnet</span><span class="sxs-lookup"><span data-stu-id="cf733-137">-Subnets</span></span>
<span data-ttu-id="cf733-138">Specifica una matrice di subnet in cui questo cmdlet distribuisce il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="cf733-139">Non è possibile aggiornare le subnet mentre il gateway dell'applicazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cf733-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="cf733-140">Per arrestare il gateway dell'applicazione, usare il cmdlet Stop-AzureApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="cf733-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf733-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="cf733-141">-VnetName</span></span>
<span data-ttu-id="cf733-142">Specifica la rete virtuale in cui questo cmdlet distribuisce il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf733-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="cf733-143">Non è possibile aggiornare una rete virtuale mentre il gateway dell'applicazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cf733-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="cf733-144">Per arrestare il gateway dell'applicazione, usare **Stop-AzureApplicationGateway**.</span><span class="sxs-lookup"><span data-stu-id="cf733-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

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

### <span data-ttu-id="cf733-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf733-145">CommonParameters</span></span>
<span data-ttu-id="cf733-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf733-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf733-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf733-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf733-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf733-148">INPUTS</span></span>

### <span data-ttu-id="cf733-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cf733-149">System.String</span></span>

## <span data-ttu-id="cf733-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf733-150">OUTPUTS</span></span>

### <span data-ttu-id="cf733-151">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cf733-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="cf733-152">Note</span><span class="sxs-lookup"><span data-stu-id="cf733-152">NOTES</span></span>

## <span data-ttu-id="cf733-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf733-153">RELATED LINKS</span></span>

[<span data-ttu-id="cf733-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf733-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="cf733-155">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf733-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="cf733-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf733-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="cf733-157">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf733-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="cf733-158">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf733-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

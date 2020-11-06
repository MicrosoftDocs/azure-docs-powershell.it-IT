---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
ms.openlocfilehash: 65d319749424697c882012d23bf12f87f92adbc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520912"
---
# <span data-ttu-id="66036-101">Remove-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="66036-101">Remove-AzureRmVirtualHub</span></span>

## <span data-ttu-id="66036-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66036-102">SYNOPSIS</span></span>
<span data-ttu-id="66036-103">Rimuove una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="66036-103">Removes an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66036-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66036-104">SYNTAX</span></span>

### <span data-ttu-id="66036-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66036-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66036-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="66036-106">ByVirtualHubResourceId</span></span>
```
Remove-AzureRmVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66036-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="66036-107">ByVirtualHubObject</span></span>
```
Remove-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66036-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66036-108">DESCRIPTION</span></span>
<span data-ttu-id="66036-109">Rimuove una risorsa di Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="66036-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="66036-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66036-110">EXAMPLES</span></span>

### <span data-ttu-id="66036-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="66036-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="66036-112">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="66036-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="66036-113">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="66036-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="66036-114">Quindi Elimina l'hub virtuale usando il relativo ResourceGroupName e il resourceName.</span><span class="sxs-lookup"><span data-stu-id="66036-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="66036-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="66036-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="66036-116">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="66036-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="66036-117">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="66036-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="66036-118">Quindi Elimina l'hub virtuale usando un oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="66036-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="66036-119">L'oggetto di input è di tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="66036-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="66036-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="66036-120">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzureRmVirtualHub
```

<span data-ttu-id="66036-121">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="66036-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="66036-122">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="66036-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="66036-123">Elimina quindi l'hub virtuale usando il piping di PowerShell usando l'output di Get-AzureRmVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="66036-123">It then deletes the virtual hub using powershell piping using output from Get-AzureRmVirtualHub.</span></span>

## <span data-ttu-id="66036-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66036-124">PARAMETERS</span></span>

### <span data-ttu-id="66036-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66036-125">-AsJob</span></span>
<span data-ttu-id="66036-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="66036-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66036-127">-DefaultProfile</span></span>
<span data-ttu-id="66036-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66036-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-129">-Force</span><span class="sxs-lookup"><span data-stu-id="66036-129">-Force</span></span>
<span data-ttu-id="66036-130">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="66036-130">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66036-131">-InputObject</span></span>
<span data-ttu-id="66036-132">L'oggetto hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="66036-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66036-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="66036-133">-Name</span></span>
<span data-ttu-id="66036-134">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="66036-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66036-135">-PassThru</span></span>
<span data-ttu-id="66036-136">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="66036-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66036-137">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="66036-137">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66036-138">-ResourceGroupName</span></span>
<span data-ttu-id="66036-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66036-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66036-140">-ResourceId</span></span>
<span data-ttu-id="66036-141">ID risorsa dell'hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="66036-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66036-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66036-142">-Confirm</span></span>
<span data-ttu-id="66036-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66036-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66036-144">-WhatIf</span></span>
<span data-ttu-id="66036-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66036-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66036-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66036-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66036-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66036-147">CommonParameters</span></span>
<span data-ttu-id="66036-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66036-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66036-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66036-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66036-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66036-150">INPUTS</span></span>

### <span data-ttu-id="66036-151">System. String</span><span class="sxs-lookup"><span data-stu-id="66036-151">System.String</span></span>

### <span data-ttu-id="66036-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="66036-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="66036-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66036-153">OUTPUTS</span></span>

### <span data-ttu-id="66036-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66036-154">System.Boolean</span></span>

## <span data-ttu-id="66036-155">Note</span><span class="sxs-lookup"><span data-stu-id="66036-155">NOTES</span></span>

## <span data-ttu-id="66036-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66036-156">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186926"
---
# <span data-ttu-id="c8799-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c8799-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="c8799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8799-102">SYNOPSIS</span></span>
<span data-ttu-id="c8799-103">Rimuove una risorsa Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c8799-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="c8799-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8799-104">SYNTAX</span></span>

### <span data-ttu-id="c8799-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8799-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8799-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c8799-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8799-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c8799-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8799-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8799-108">DESCRIPTION</span></span>
<span data-ttu-id="c8799-109">Rimuove una risorsa Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c8799-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="c8799-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8799-110">EXAMPLES</span></span>

### <span data-ttu-id="c8799-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8799-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="c8799-112">La procedura precedente consente di creare un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale negli Stati Uniti occidentali in quel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="c8799-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c8799-113">L'hub virtuale avrà lo spazio di indirizzi "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c8799-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c8799-114">L'hub virtuale viene quindi eliminato usando i nomi ResourceGroupName e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="c8799-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="c8799-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c8799-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="c8799-116">La procedura precedente consente di creare un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale negli Stati Uniti occidentali in quel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="c8799-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c8799-117">L'hub virtuale avrà lo spazio di indirizzi "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c8799-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c8799-118">L'hub virtuale viene quindi eliminato usando un oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="c8799-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="c8799-119">L'oggetto di input è di tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c8799-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="c8799-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c8799-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="c8799-121">La procedura precedente consente di creare un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale negli Stati Uniti occidentali in quel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="c8799-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c8799-122">L'hub virtuale avrà lo spazio di indirizzi "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c8799-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c8799-123">L'hub virtuale viene quindi eliminato usando le funzionalità di piping di PowerShell con l'output di Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c8799-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="c8799-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8799-124">PARAMETERS</span></span>

### <span data-ttu-id="c8799-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8799-125">-AsJob</span></span>
<span data-ttu-id="c8799-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c8799-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8799-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8799-127">-DefaultProfile</span></span>
<span data-ttu-id="c8799-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8799-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8799-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c8799-129">-Force</span></span>
<span data-ttu-id="c8799-130">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="c8799-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c8799-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8799-131">-InputObject</span></span>
<span data-ttu-id="c8799-132">L'oggetto hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="c8799-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="c8799-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c8799-133">-Name</span></span>
<span data-ttu-id="c8799-134">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c8799-134">The resource name.</span></span>

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

### <span data-ttu-id="c8799-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8799-135">-PassThru</span></span>
<span data-ttu-id="c8799-136">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c8799-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8799-137">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c8799-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8799-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8799-138">-ResourceGroupName</span></span>
<span data-ttu-id="c8799-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c8799-139">The resource group name.</span></span>

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

### <span data-ttu-id="c8799-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8799-140">-ResourceId</span></span>
<span data-ttu-id="c8799-141">ID risorsa dell'hub virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="c8799-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="c8799-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8799-142">-Confirm</span></span>
<span data-ttu-id="c8799-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8799-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8799-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8799-144">-WhatIf</span></span>
<span data-ttu-id="c8799-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8799-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8799-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8799-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8799-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8799-147">CommonParameters</span></span>
<span data-ttu-id="c8799-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8799-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8799-149">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8799-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8799-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8799-150">INPUTS</span></span>

### <span data-ttu-id="c8799-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c8799-151">System.String</span></span>

### <span data-ttu-id="c8799-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c8799-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c8799-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8799-153">OUTPUTS</span></span>

### <span data-ttu-id="c8799-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8799-154">System.Boolean</span></span>

## <span data-ttu-id="c8799-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8799-155">NOTES</span></span>

## <span data-ttu-id="c8799-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8799-156">RELATED LINKS</span></span>

[<span data-ttu-id="c8799-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c8799-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="c8799-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c8799-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="c8799-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c8799-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

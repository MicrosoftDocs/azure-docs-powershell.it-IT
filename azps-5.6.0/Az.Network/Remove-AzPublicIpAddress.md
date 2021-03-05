---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: f8a509fc73387361de5bd191ee9eefc61c33a5f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996126"
---
# <span data-ttu-id="ce6a8-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ce6a8-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="ce6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6a8-103">Rimuove un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-103">Removes a public IP address.</span></span>

## <span data-ttu-id="ce6a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce6a8-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce6a8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce6a8-105">DESCRIPTION</span></span>
<span data-ttu-id="ce6a8-106">Il cmdlet **Remove-AzPublicIpAddress** rimuove un indirizzo IP pubblico di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="ce6a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce6a8-107">EXAMPLES</span></span>

### <span data-ttu-id="ce6a8-108">1: Rimuovere una risorsa indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ce6a8-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="ce6a8-109">Questo comando rimuove la risorsa indirizzo IP pubblico denominata $publicIpName nel gruppo di $rgName.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="ce6a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce6a8-110">PARAMETERS</span></span>

### <span data-ttu-id="ce6a8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce6a8-111">-AsJob</span></span>
<span data-ttu-id="ce6a8-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ce6a8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce6a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6a8-113">-DefaultProfile</span></span>
<span data-ttu-id="ce6a8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce6a8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ce6a8-115">-Force</span></span>
<span data-ttu-id="ce6a8-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce6a8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ce6a8-117">-Name</span></span>
<span data-ttu-id="ce6a8-118">Specifica il nome dell'indirizzo IP pubblico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6a8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce6a8-119">-PassThru</span></span>
<span data-ttu-id="ce6a8-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce6a8-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce6a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce6a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce6a8-123">Specifica il nome del gruppo di risorse che contiene l'indirizzo IP pubblico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6a8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce6a8-124">-Confirm</span></span>
<span data-ttu-id="ce6a8-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6a8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce6a8-126">-WhatIf</span></span>
<span data-ttu-id="ce6a8-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce6a8-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6a8-129">CommonParameters</span></span>
<span data-ttu-id="ce6a8-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce6a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6a8-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce6a8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6a8-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce6a8-132">INPUTS</span></span>

### <span data-ttu-id="ce6a8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ce6a8-133">System.String</span></span>

## <span data-ttu-id="ce6a8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce6a8-134">OUTPUTS</span></span>

### <span data-ttu-id="ce6a8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce6a8-135">System.Boolean</span></span>

## <span data-ttu-id="ce6a8-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce6a8-136">NOTES</span></span>

## <span data-ttu-id="ce6a8-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce6a8-137">RELATED LINKS</span></span>

[<span data-ttu-id="ce6a8-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ce6a8-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="ce6a8-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ce6a8-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ce6a8-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ce6a8-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488952"
---
# <span data-ttu-id="3a6fa-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a6fa-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="3a6fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6fa-103">Rimuove un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-103">Removes a public IP address.</span></span>

## <span data-ttu-id="3a6fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a6fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a6fa-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6fa-106">Il cmdlet **Remove-AzPublicIpAddress** rimuove un indirizzo IP pubblico di Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="3a6fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-107">EXAMPLES</span></span>

### <span data-ttu-id="3a6fa-108">1: rimuovere una risorsa indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="3a6fa-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="3a6fa-109">Questo comando rimuove la risorsa indirizzo IP pubblico denominata $publicIpName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="3a6fa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-110">PARAMETERS</span></span>

### <span data-ttu-id="3a6fa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a6fa-111">-AsJob</span></span>
<span data-ttu-id="3a6fa-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3a6fa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a6fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6fa-113">-DefaultProfile</span></span>
<span data-ttu-id="3a6fa-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a6fa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3a6fa-115">-Force</span></span>
<span data-ttu-id="3a6fa-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a6fa-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a6fa-117">-Name</span></span>
<span data-ttu-id="3a6fa-118">Specifica il nome dell'indirizzo IP pubblico rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a6fa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a6fa-119">-PassThru</span></span>
<span data-ttu-id="3a6fa-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a6fa-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a6fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a6fa-123">Specifica il nome del gruppo di risorse che contiene l'indirizzo IP pubblico rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a6fa-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a6fa-124">-Confirm</span></span>
<span data-ttu-id="3a6fa-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a6fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6fa-126">-WhatIf</span></span>
<span data-ttu-id="3a6fa-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a6fa-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6fa-129">CommonParameters</span></span>
<span data-ttu-id="3a6fa-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6fa-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6fa-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6fa-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-132">INPUTS</span></span>

### <span data-ttu-id="3a6fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3a6fa-133">System.String</span></span>

## <span data-ttu-id="3a6fa-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a6fa-134">OUTPUTS</span></span>

### <span data-ttu-id="3a6fa-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a6fa-135">System.Boolean</span></span>

## <span data-ttu-id="3a6fa-136">Note</span><span class="sxs-lookup"><span data-stu-id="3a6fa-136">NOTES</span></span>

## <span data-ttu-id="3a6fa-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a6fa-137">RELATED LINKS</span></span>

[<span data-ttu-id="3a6fa-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a6fa-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="3a6fa-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a6fa-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="3a6fa-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a6fa-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)



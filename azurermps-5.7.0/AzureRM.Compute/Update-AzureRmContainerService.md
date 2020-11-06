---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: 62acfacbafb50f85673b37e802b9d0b0eb4bf66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508291"
---
# <span data-ttu-id="c3beb-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c3beb-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="c3beb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3beb-102">SYNOPSIS</span></span>
<span data-ttu-id="c3beb-103">Aggiorna lo stato di un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="c3beb-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3beb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3beb-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3beb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3beb-105">DESCRIPTION</span></span>
<span data-ttu-id="c3beb-106">Il cmdlet **Update-AzureRmContainerService** aggiorna lo stato di un servizio contenitore in base a un'istanza locale del servizio.</span><span class="sxs-lookup"><span data-stu-id="c3beb-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="c3beb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3beb-107">EXAMPLES</span></span>

### <span data-ttu-id="c3beb-108">Esempio 1: aggiornare un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="c3beb-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="c3beb-109">Questo comando ottiene il servizio contenitore denominato CSResourceGroup17 usando il cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="c3beb-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="c3beb-110">Il comando passa l'oggetto al cmdlet Remove-AzureRmContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3beb-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="c3beb-111">**Remove-AzureRmContainerServiceAgentPoolProfile** rimuove il profilo denominato AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="c3beb-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="c3beb-112">Il comando passa il risultato al cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="c3beb-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="c3beb-113">**Add-AzureRmContainerServiceAgentPoolProfile** aggiunge un profilo con il nome AgentPool01 e ha le proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="c3beb-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="c3beb-114">Il comando passa il risultato al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="c3beb-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="c3beb-115">Il cmdlet corrente aggiorna il servizio contenitore per riflettere le modifiche apportate in questo comando.</span><span class="sxs-lookup"><span data-stu-id="c3beb-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="c3beb-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3beb-116">PARAMETERS</span></span>

### <span data-ttu-id="c3beb-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="c3beb-117">-ContainerService</span></span>
<span data-ttu-id="c3beb-118">Specifica un oggetto **ContainerService** locale che contiene le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c3beb-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3beb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3beb-119">-Name</span></span>
<span data-ttu-id="c3beb-120">Specifica il nome del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="c3beb-120">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3beb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3beb-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3beb-122">Specifica il gruppo di risorse del servizio contenitore che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="c3beb-122">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3beb-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3beb-123">-Confirm</span></span>
<span data-ttu-id="c3beb-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3beb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3beb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3beb-125">-WhatIf</span></span>
<span data-ttu-id="c3beb-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3beb-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c3beb-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3beb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3beb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3beb-128">CommonParameters</span></span>
<span data-ttu-id="c3beb-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3beb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3beb-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3beb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3beb-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3beb-131">INPUTS</span></span>

### <span data-ttu-id="c3beb-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3beb-132">None</span></span>
<span data-ttu-id="c3beb-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c3beb-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3beb-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3beb-134">OUTPUTS</span></span>

## <span data-ttu-id="c3beb-135">Note</span><span class="sxs-lookup"><span data-stu-id="c3beb-135">NOTES</span></span>

## <span data-ttu-id="c3beb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3beb-136">RELATED LINKS</span></span>

[<span data-ttu-id="c3beb-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="c3beb-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="c3beb-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c3beb-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="c3beb-139">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c3beb-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="c3beb-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c3beb-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="c3beb-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="c3beb-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)



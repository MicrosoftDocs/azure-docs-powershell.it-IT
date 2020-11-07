---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685627"
---
# <span data-ttu-id="71e52-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="71e52-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="71e52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71e52-102">SYNOPSIS</span></span>
<span data-ttu-id="71e52-103">Rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="71e52-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71e52-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71e52-105">DESCRIPTION</span></span>
<span data-ttu-id="71e52-106">Il cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** rimuove un profilo del pool di agenti da un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="71e52-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="71e52-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71e52-107">EXAMPLES</span></span>

### <span data-ttu-id="71e52-108">Esempio 1: rimuovere un profilo da un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="71e52-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="71e52-109">Il primo comando ottiene un servizio contenitore denominato CSResourceGroup17 tramite il cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="71e52-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="71e52-110">Il comando Archivia il servizio nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="71e52-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="71e52-111">Il secondo comando rimuove il profilo denominato AgentPool01 dal servizio contenitore in $Container.</span><span class="sxs-lookup"><span data-stu-id="71e52-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="71e52-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71e52-112">PARAMETERS</span></span>

### <span data-ttu-id="71e52-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="71e52-113">-ContainerService</span></span>
<span data-ttu-id="71e52-114">Specifica l'oggetto servizio contenitore da cui questo cmdlet rimuove un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="71e52-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e52-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="71e52-115">-Name</span></span>
<span data-ttu-id="71e52-116">Specifica il nome del profilo del pool di agenti rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e52-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71e52-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71e52-117">-Confirm</span></span>
<span data-ttu-id="71e52-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e52-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e52-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e52-119">-WhatIf</span></span>
<span data-ttu-id="71e52-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71e52-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71e52-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71e52-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e52-122">CommonParameters</span></span>
<span data-ttu-id="71e52-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e52-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e52-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e52-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71e52-125">INPUTS</span></span>

### <span data-ttu-id="71e52-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="71e52-126">None</span></span>
<span data-ttu-id="71e52-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="71e52-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71e52-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71e52-128">OUTPUTS</span></span>

## <span data-ttu-id="71e52-129">Note</span><span class="sxs-lookup"><span data-stu-id="71e52-129">NOTES</span></span>

## <span data-ttu-id="71e52-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71e52-130">RELATED LINKS</span></span>

[<span data-ttu-id="71e52-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="71e52-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="71e52-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="71e52-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)



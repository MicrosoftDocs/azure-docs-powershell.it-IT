---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: fc66151f39c969ebbdc9b54d6f6ed97db909e05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688029"
---
# <span data-ttu-id="e1d6f-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e1d6f-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="e1d6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d6f-103">Rimuove un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1d6f-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d6f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d6f-106">Il cmdlet **Remove-AzureRmContainerService** rimuove un servizio contenitore dall'account Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="e1d6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d6f-108">Esempio 1: rimuovere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="e1d6f-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="e1d6f-109">Questo comando rimuove il servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="e1d6f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1d6f-110">PARAMETERS</span></span>

### <span data-ttu-id="e1d6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d6f-111">-DefaultProfile</span></span>
<span data-ttu-id="e1d6f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d6f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e1d6f-113">-Force</span></span>
<span data-ttu-id="e1d6f-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1d6f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1d6f-115">-Name</span></span>
<span data-ttu-id="e1d6f-116">Specifica il nome del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-116">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d6f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d6f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1d6f-118">Specifica il gruppo di risorse del servizio contenitore rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-118">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d6f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1d6f-119">-Confirm</span></span>
<span data-ttu-id="e1d6f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-120">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="e1d6f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d6f-121">-WhatIf</span></span>
<span data-ttu-id="e1d6f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1d6f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-123">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="e1d6f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d6f-124">CommonParameters</span></span>
<span data-ttu-id="e1d6f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d6f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d6f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d6f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d6f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1d6f-127">INPUTS</span></span>

## <span data-ttu-id="e1d6f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1d6f-128">OUTPUTS</span></span>

## <span data-ttu-id="e1d6f-129">Note</span><span class="sxs-lookup"><span data-stu-id="e1d6f-129">NOTES</span></span>

## <span data-ttu-id="e1d6f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1d6f-130">RELATED LINKS</span></span>

[<span data-ttu-id="e1d6f-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e1d6f-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="e1d6f-132">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e1d6f-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="e1d6f-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e1d6f-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)



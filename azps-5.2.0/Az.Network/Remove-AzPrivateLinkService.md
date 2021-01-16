---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369249"
---
# <span data-ttu-id="8bb36-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8bb36-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="8bb36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bb36-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb36-103">Rimuove un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="8bb36-103">Removes a private link service</span></span>

## <span data-ttu-id="8bb36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bb36-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bb36-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bb36-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb36-106">Il cmdlet **Remove-AzPrivateLinkService** rimuove un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="8bb36-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="8bb36-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bb36-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb36-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8bb36-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="8bb36-109">In questo esempio viene rimosso un servizio di collegamento privato denominato TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8bb36-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="8bb36-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bb36-110">PARAMETERS</span></span>

### <span data-ttu-id="8bb36-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bb36-111">-AsJob</span></span>
<span data-ttu-id="8bb36-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8bb36-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bb36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb36-113">-DefaultProfile</span></span>
<span data-ttu-id="8bb36-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bb36-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8bb36-115">-Force</span></span>
<span data-ttu-id="8bb36-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="8bb36-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8bb36-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bb36-117">-Name</span></span>
<span data-ttu-id="8bb36-118">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="8bb36-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb36-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bb36-119">-PassThru</span></span>
<span data-ttu-id="8bb36-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8bb36-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8bb36-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8bb36-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8bb36-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb36-122">-ResourceGroupName</span></span>
<span data-ttu-id="8bb36-123">Il nome del gruppo di risorse del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="8bb36-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="8bb36-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bb36-124">-Confirm</span></span>
<span data-ttu-id="8bb36-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bb36-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb36-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb36-126">-WhatIf</span></span>
<span data-ttu-id="8bb36-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bb36-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb36-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bb36-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb36-129">CommonParameters</span></span>
<span data-ttu-id="8bb36-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb36-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bb36-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb36-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bb36-132">INPUTS</span></span>

### <span data-ttu-id="8bb36-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8bb36-133">System.String</span></span>

## <span data-ttu-id="8bb36-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bb36-134">OUTPUTS</span></span>

### <span data-ttu-id="8bb36-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bb36-135">System.Boolean</span></span>

## <span data-ttu-id="8bb36-136">Note</span><span class="sxs-lookup"><span data-stu-id="8bb36-136">NOTES</span></span>

## <span data-ttu-id="8bb36-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bb36-137">RELATED LINKS</span></span>

[<span data-ttu-id="8bb36-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8bb36-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="8bb36-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8bb36-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)
---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516435"
---
# <span data-ttu-id="633dc-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="633dc-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="633dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="633dc-102">SYNOPSIS</span></span>
<span data-ttu-id="633dc-103">Rigenerare un tasto di accesso per un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="633dc-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="633dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="633dc-104">SYNTAX</span></span>

### <span data-ttu-id="633dc-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="633dc-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633dc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="633dc-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633dc-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="633dc-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="633dc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="633dc-108">DESCRIPTION</span></span>
<span data-ttu-id="633dc-109">Rigenerare un tasto di accesso per un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="633dc-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="633dc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="633dc-110">EXAMPLES</span></span>

### <span data-ttu-id="633dc-111">Rigenerare la chiave primaria</span><span class="sxs-lookup"><span data-stu-id="633dc-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="633dc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="633dc-112">PARAMETERS</span></span>

### <span data-ttu-id="633dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633dc-113">-DefaultProfile</span></span>
<span data-ttu-id="633dc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="633dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="633dc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="633dc-115">-InputObject</span></span>
<span data-ttu-id="633dc-116">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="633dc-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="633dc-117">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="633dc-117">-KeyType</span></span>
<span data-ttu-id="633dc-118">Il tipo di chiave, primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="633dc-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633dc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="633dc-119">-Name</span></span>
<span data-ttu-id="633dc-120">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="633dc-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633dc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="633dc-121">-PassThru</span></span>
<span data-ttu-id="633dc-122">Restituisce vero se la rigenerazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="633dc-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="633dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="633dc-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="633dc-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633dc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="633dc-125">-ResourceId</span></span>
<span data-ttu-id="633dc-126">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="633dc-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="633dc-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="633dc-127">-Confirm</span></span>
<span data-ttu-id="633dc-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="633dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="633dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="633dc-129">-WhatIf</span></span>
<span data-ttu-id="633dc-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="633dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="633dc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="633dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="633dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633dc-132">CommonParameters</span></span>
<span data-ttu-id="633dc-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="633dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633dc-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="633dc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633dc-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="633dc-135">INPUTS</span></span>

### <span data-ttu-id="633dc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="633dc-136">System.String</span></span>
<span data-ttu-id="633dc-137">Parametri: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="633dc-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="633dc-138">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="633dc-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="633dc-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="633dc-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="633dc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="633dc-140">OUTPUTS</span></span>

### <span data-ttu-id="633dc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="633dc-141">System.Boolean</span></span>

## <span data-ttu-id="633dc-142">Note</span><span class="sxs-lookup"><span data-stu-id="633dc-142">NOTES</span></span>

## <span data-ttu-id="633dc-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="633dc-143">RELATED LINKS</span></span>

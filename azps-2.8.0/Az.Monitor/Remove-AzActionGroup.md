---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: c026d161c0d5a3ac73d2736d19422ce45b59fbd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854045"
---
# <span data-ttu-id="8db63-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8db63-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="8db63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8db63-102">SYNOPSIS</span></span>
<span data-ttu-id="8db63-103">Rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="8db63-103">Removes an action group.</span></span>

## <span data-ttu-id="8db63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8db63-104">SYNTAX</span></span>

### <span data-ttu-id="8db63-105">ByPropertyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8db63-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db63-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8db63-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8db63-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8db63-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db63-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8db63-108">DESCRIPTION</span></span>
<span data-ttu-id="8db63-109">Il cmdlet **Remove-AzActionGroup** rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="8db63-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="8db63-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8db63-110">EXAMPLES</span></span>

### <span data-ttu-id="8db63-111">Esempio 1: rimuovere un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="8db63-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="8db63-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8db63-112">PARAMETERS</span></span>

### <span data-ttu-id="8db63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db63-113">-DefaultProfile</span></span>
<span data-ttu-id="8db63-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8db63-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8db63-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8db63-115">-InputObject</span></span>
<span data-ttu-id="8db63-116">Risorsa gruppo azioni</span><span class="sxs-lookup"><span data-stu-id="8db63-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8db63-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8db63-117">-Name</span></span>
<span data-ttu-id="8db63-118">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="8db63-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db63-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db63-119">-ResourceGroupName</span></span>
<span data-ttu-id="8db63-120">Gruppo risorse Nam</span><span class="sxs-lookup"><span data-stu-id="8db63-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db63-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8db63-121">-ResourceId</span></span>
<span data-ttu-id="8db63-122">Risorsa i</span><span class="sxs-lookup"><span data-stu-id="8db63-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db63-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8db63-123">-Confirm</span></span>
<span data-ttu-id="8db63-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8db63-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db63-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db63-125">-WhatIf</span></span>
<span data-ttu-id="8db63-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8db63-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8db63-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8db63-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db63-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db63-128">CommonParameters</span></span>
<span data-ttu-id="8db63-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db63-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db63-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8db63-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db63-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8db63-131">INPUTS</span></span>

### <span data-ttu-id="8db63-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8db63-132">System.String</span></span>

### <span data-ttu-id="8db63-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="8db63-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="8db63-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8db63-134">OUTPUTS</span></span>

### <span data-ttu-id="8db63-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8db63-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8db63-136">Note</span><span class="sxs-lookup"><span data-stu-id="8db63-136">NOTES</span></span>

## <span data-ttu-id="8db63-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8db63-137">RELATED LINKS</span></span>

<span data-ttu-id="8db63-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="8db63-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>

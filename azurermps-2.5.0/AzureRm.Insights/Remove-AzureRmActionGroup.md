---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7ec50b0698017c20fb47030ccb571d6b4083b97b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866346"
---
# <span data-ttu-id="0c3d9-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="0c3d9-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="0c3d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3d9-103">Rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="0c3d9-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c3d9-104">SYNTAX</span></span>

### <span data-ttu-id="0c3d9-105">ByPropertyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c3d9-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3d9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c3d9-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c3d9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c3d9-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3d9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c3d9-108">DESCRIPTION</span></span>
<span data-ttu-id="0c3d9-109">Il cmdlet **Remove-AzureRmActionGroup** rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="0c3d9-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="0c3d9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c3d9-110">EXAMPLES</span></span>

### <span data-ttu-id="0c3d9-111">Esempio 1: rimuovere un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="0c3d9-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="0c3d9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c3d9-112">PARAMETERS</span></span>

### <span data-ttu-id="0c3d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3d9-113">-DefaultProfile</span></span>
<span data-ttu-id="0c3d9-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c3d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c3d9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c3d9-115">-InputObject</span></span>
<span data-ttu-id="0c3d9-116">Gruppo di azioni resourc</span><span class="sxs-lookup"><span data-stu-id="0c3d9-116">The action group resourc</span></span>

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

### <span data-ttu-id="0c3d9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c3d9-117">-Name</span></span>
<span data-ttu-id="0c3d9-118">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="0c3d9-118">The name of the action group.</span></span>

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

### <span data-ttu-id="0c3d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c3d9-120">Gruppo risorse Nam</span><span class="sxs-lookup"><span data-stu-id="0c3d9-120">The resource group nam</span></span>

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

### <span data-ttu-id="0c3d9-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c3d9-121">-ResourceId</span></span>
<span data-ttu-id="0c3d9-122">Risorsa i</span><span class="sxs-lookup"><span data-stu-id="0c3d9-122">The resource i</span></span>

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

### <span data-ttu-id="0c3d9-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c3d9-123">-Confirm</span></span>
<span data-ttu-id="0c3d9-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c3d9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3d9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3d9-125">-WhatIf</span></span>
<span data-ttu-id="0c3d9-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c3d9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c3d9-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c3d9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3d9-128">CommonParameters</span></span>
<span data-ttu-id="0c3d9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3d9-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3d9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3d9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c3d9-131">INPUTS</span></span>

### <span data-ttu-id="0c3d9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0c3d9-132">System.String</span></span>

### <span data-ttu-id="0c3d9-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="0c3d9-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="0c3d9-134">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c3d9-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0c3d9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c3d9-135">OUTPUTS</span></span>

### <span data-ttu-id="0c3d9-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0c3d9-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0c3d9-137">Note</span><span class="sxs-lookup"><span data-stu-id="0c3d9-137">NOTES</span></span>

## <span data-ttu-id="0c3d9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c3d9-138">RELATED LINKS</span></span>

<span data-ttu-id="0c3d9-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="0c3d9-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>

---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 0b5f84a38fcd087b77b32624b9cbd9b3b8a27e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688019"
---
# <span data-ttu-id="f3220-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="f3220-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="f3220-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3220-102">SYNOPSIS</span></span>
<span data-ttu-id="f3220-103">Rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="f3220-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3220-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3220-104">SYNTAX</span></span>

### <span data-ttu-id="f3220-105">ByPropertyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3220-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3220-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3220-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3220-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f3220-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3220-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3220-108">DESCRIPTION</span></span>
<span data-ttu-id="f3220-109">Il cmdlet **Remove-AzureRmActionGroup** rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="f3220-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="f3220-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3220-110">EXAMPLES</span></span>

### <span data-ttu-id="f3220-111">Esempio 1: rimuovere un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="f3220-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="f3220-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3220-112">PARAMETERS</span></span>

### <span data-ttu-id="f3220-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3220-113">-Name</span></span>
<span data-ttu-id="f3220-114">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="f3220-114">The name of the action group.</span></span>

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

### <span data-ttu-id="f3220-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f3220-115">-Confirm</span></span>
<span data-ttu-id="f3220-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3220-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3220-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3220-117">-DefaultProfile</span></span>
<span data-ttu-id="f3220-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3220-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3220-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3220-119">-InputObject</span></span>
<span data-ttu-id="f3220-120">Risorsa gruppo azioni</span><span class="sxs-lookup"><span data-stu-id="f3220-120">The action group resource</span></span>

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

### <span data-ttu-id="f3220-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3220-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3220-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f3220-122">The resource group name</span></span>

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

### <span data-ttu-id="f3220-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3220-123">-ResourceId</span></span>
<span data-ttu-id="f3220-124">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="f3220-124">The resource id</span></span>

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

### <span data-ttu-id="f3220-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3220-125">-WhatIf</span></span>
<span data-ttu-id="f3220-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3220-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3220-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3220-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3220-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3220-128">CommonParameters</span></span>
<span data-ttu-id="f3220-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3220-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3220-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3220-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3220-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3220-131">INPUTS</span></span>

## <span data-ttu-id="f3220-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3220-132">OUTPUTS</span></span>

### <span data-ttu-id="f3220-133">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f3220-133">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f3220-134">Note</span><span class="sxs-lookup"><span data-stu-id="f3220-134">NOTES</span></span>

## <span data-ttu-id="f3220-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3220-135">RELATED LINKS</span></span>

<span data-ttu-id="f3220-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="f3220-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>

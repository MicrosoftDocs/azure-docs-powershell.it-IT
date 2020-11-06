---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519457"
---
# <span data-ttu-id="20fd1-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="20fd1-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="20fd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="20fd1-103">Rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="20fd1-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20fd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20fd1-104">SYNTAX</span></span>

### <span data-ttu-id="20fd1-105">ByPropertyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20fd1-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fd1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="20fd1-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20fd1-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="20fd1-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20fd1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20fd1-108">DESCRIPTION</span></span>
<span data-ttu-id="20fd1-109">Il cmdlet **Remove-AzureRmActionGroup** rimuove un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="20fd1-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="20fd1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20fd1-110">EXAMPLES</span></span>

### <span data-ttu-id="20fd1-111">Esempio 1: rimuovere un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="20fd1-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="20fd1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20fd1-112">PARAMETERS</span></span>

### <span data-ttu-id="20fd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fd1-113">-DefaultProfile</span></span>
<span data-ttu-id="20fd1-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="20fd1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fd1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20fd1-115">-InputObject</span></span>
<span data-ttu-id="20fd1-116">Gruppo di azioni resourc</span><span class="sxs-lookup"><span data-stu-id="20fd1-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20fd1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="20fd1-117">-Name</span></span>
<span data-ttu-id="20fd1-118">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="20fd1-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fd1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fd1-119">-ResourceGroupName</span></span>
<span data-ttu-id="20fd1-120">Gruppo risorse Nam</span><span class="sxs-lookup"><span data-stu-id="20fd1-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fd1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20fd1-121">-ResourceId</span></span>
<span data-ttu-id="20fd1-122">Risorsa i</span><span class="sxs-lookup"><span data-stu-id="20fd1-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fd1-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="20fd1-123">-Confirm</span></span>
<span data-ttu-id="20fd1-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20fd1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20fd1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20fd1-125">-WhatIf</span></span>
<span data-ttu-id="20fd1-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20fd1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20fd1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20fd1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20fd1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fd1-128">CommonParameters</span></span>
<span data-ttu-id="20fd1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20fd1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fd1-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20fd1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fd1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20fd1-131">INPUTS</span></span>

### <span data-ttu-id="20fd1-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="20fd1-132">None</span></span>
<span data-ttu-id="20fd1-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="20fd1-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20fd1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20fd1-134">OUTPUTS</span></span>

### <span data-ttu-id="20fd1-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="20fd1-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="20fd1-136">Note</span><span class="sxs-lookup"><span data-stu-id="20fd1-136">NOTES</span></span>

## <span data-ttu-id="20fd1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20fd1-137">RELATED LINKS</span></span>

<span data-ttu-id="20fd1-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="20fd1-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>

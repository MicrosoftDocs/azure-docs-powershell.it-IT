---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 8b7603f145d45411b20b124823f28281d4117127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685682"
---
# <span data-ttu-id="2e83c-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="2e83c-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="2e83c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e83c-102">SYNOPSIS</span></span>
<span data-ttu-id="2e83c-103">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="2e83c-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e83c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e83c-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e83c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e83c-105">DESCRIPTION</span></span>
<span data-ttu-id="2e83c-106">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="2e83c-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="2e83c-107">Se sono presenti più tasti con lo stesso nome, la prima nell'elenco viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="2e83c-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="2e83c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e83c-108">EXAMPLES</span></span>

### <span data-ttu-id="2e83c-109">Esempio 1 eliminare un IotHub</span><span class="sxs-lookup"><span data-stu-id="2e83c-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="2e83c-110">Rimuove la chiave denominata iothubowner1 dalla IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2e83c-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2e83c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e83c-111">PARAMETERS</span></span>

### <span data-ttu-id="2e83c-112">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="2e83c-112">-KeyName</span></span>
<span data-ttu-id="2e83c-113">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="2e83c-113">Name of the Key</span></span>

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

### <span data-ttu-id="2e83c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e83c-114">-Name</span></span>
<span data-ttu-id="2e83c-115">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="2e83c-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="2e83c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e83c-116">-ResourceGroupName</span></span>
<span data-ttu-id="2e83c-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2e83c-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e83c-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e83c-118">-Confirm</span></span>
<span data-ttu-id="2e83c-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e83c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e83c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e83c-120">-WhatIf</span></span>
<span data-ttu-id="2e83c-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e83c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e83c-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e83c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e83c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e83c-123">-DefaultProfile</span></span>
<span data-ttu-id="2e83c-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e83c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e83c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e83c-125">CommonParameters</span></span>
<span data-ttu-id="2e83c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e83c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e83c-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e83c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e83c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e83c-128">INPUTS</span></span>

### <span data-ttu-id="2e83c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2e83c-129">System.String</span></span>

## <span data-ttu-id="2e83c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e83c-130">OUTPUTS</span></span>

### <span data-ttu-id="2e83c-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2e83c-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2e83c-132">Note</span><span class="sxs-lookup"><span data-stu-id="2e83c-132">NOTES</span></span>

## <span data-ttu-id="2e83c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e83c-133">RELATED LINKS</span></span>


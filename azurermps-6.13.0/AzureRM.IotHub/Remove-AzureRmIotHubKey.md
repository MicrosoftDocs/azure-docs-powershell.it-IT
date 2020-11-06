---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 0f48bf7ad03dcfd59f8ea3653acdb7a57aa5240c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510979"
---
# <span data-ttu-id="743c6-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="743c6-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="743c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="743c6-102">SYNOPSIS</span></span>
<span data-ttu-id="743c6-103">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="743c6-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="743c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="743c6-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="743c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="743c6-105">DESCRIPTION</span></span>
<span data-ttu-id="743c6-106">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="743c6-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="743c6-107">Se sono presenti più tasti con lo stesso nome, la prima nell'elenco viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="743c6-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="743c6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="743c6-108">EXAMPLES</span></span>

### <span data-ttu-id="743c6-109">Esempio 1 eliminare un IotHub</span><span class="sxs-lookup"><span data-stu-id="743c6-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="743c6-110">Rimuove la chiave denominata iothubowner1 dalla IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="743c6-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="743c6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="743c6-111">PARAMETERS</span></span>

### <span data-ttu-id="743c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743c6-112">-DefaultProfile</span></span>
<span data-ttu-id="743c6-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="743c6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="743c6-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="743c6-114">-KeyName</span></span>
<span data-ttu-id="743c6-115">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="743c6-115">Name of the Key</span></span>

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

### <span data-ttu-id="743c6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="743c6-116">-Name</span></span>
<span data-ttu-id="743c6-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="743c6-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="743c6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743c6-118">-ResourceGroupName</span></span>
<span data-ttu-id="743c6-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="743c6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="743c6-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="743c6-120">-Confirm</span></span>
<span data-ttu-id="743c6-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743c6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="743c6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="743c6-122">-WhatIf</span></span>
<span data-ttu-id="743c6-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="743c6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="743c6-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="743c6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="743c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743c6-125">CommonParameters</span></span>
<span data-ttu-id="743c6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743c6-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743c6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743c6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="743c6-128">INPUTS</span></span>

### <span data-ttu-id="743c6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="743c6-129">System.String</span></span>

## <span data-ttu-id="743c6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="743c6-130">OUTPUTS</span></span>

### <span data-ttu-id="743c6-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="743c6-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="743c6-132">Note</span><span class="sxs-lookup"><span data-stu-id="743c6-132">NOTES</span></span>

## <span data-ttu-id="743c6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="743c6-133">RELATED LINKS</span></span>

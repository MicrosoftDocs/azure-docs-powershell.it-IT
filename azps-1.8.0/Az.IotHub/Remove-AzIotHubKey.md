---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835839"
---
# <span data-ttu-id="d6317-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d6317-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="d6317-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6317-102">SYNOPSIS</span></span>
<span data-ttu-id="d6317-103">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="d6317-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="d6317-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6317-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6317-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6317-105">DESCRIPTION</span></span>
<span data-ttu-id="d6317-106">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="d6317-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="d6317-107">Se sono presenti più tasti con lo stesso nome, la prima nell'elenco viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="d6317-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="d6317-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6317-108">EXAMPLES</span></span>

### <span data-ttu-id="d6317-109">Esempio 1 eliminare un IotHub</span><span class="sxs-lookup"><span data-stu-id="d6317-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="d6317-110">Rimuove la chiave denominata iothubowner1 dalla IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d6317-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d6317-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6317-111">PARAMETERS</span></span>

### <span data-ttu-id="d6317-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6317-112">-DefaultProfile</span></span>
<span data-ttu-id="d6317-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d6317-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6317-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="d6317-114">-KeyName</span></span>
<span data-ttu-id="d6317-115">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="d6317-115">Name of the Key</span></span>

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

### <span data-ttu-id="d6317-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6317-116">-Name</span></span>
<span data-ttu-id="d6317-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="d6317-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="d6317-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6317-118">-ResourceGroupName</span></span>
<span data-ttu-id="d6317-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d6317-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d6317-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6317-120">-Confirm</span></span>
<span data-ttu-id="d6317-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6317-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6317-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6317-122">-WhatIf</span></span>
<span data-ttu-id="d6317-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6317-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6317-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6317-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6317-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6317-125">CommonParameters</span></span>
<span data-ttu-id="d6317-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6317-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6317-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6317-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6317-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6317-128">INPUTS</span></span>

### <span data-ttu-id="d6317-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d6317-129">System.String</span></span>

## <span data-ttu-id="d6317-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6317-130">OUTPUTS</span></span>

### <span data-ttu-id="d6317-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d6317-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d6317-132">Note</span><span class="sxs-lookup"><span data-stu-id="d6317-132">NOTES</span></span>

## <span data-ttu-id="d6317-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6317-133">RELATED LINKS</span></span>

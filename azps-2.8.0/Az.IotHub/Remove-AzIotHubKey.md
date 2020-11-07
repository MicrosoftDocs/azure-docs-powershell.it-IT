---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: eb0ec4390cb8e354707109ecafb5d284b70fa910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674203"
---
# <span data-ttu-id="ef38c-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ef38c-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="ef38c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef38c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef38c-103">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="ef38c-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="ef38c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef38c-104">SYNTAX</span></span>

### <span data-ttu-id="ef38c-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef38c-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef38c-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ef38c-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef38c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef38c-107">DESCRIPTION</span></span>
<span data-ttu-id="ef38c-108">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="ef38c-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="ef38c-109">Se sono presenti più tasti con lo stesso nome, la prima nell'elenco viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef38c-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="ef38c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef38c-110">EXAMPLES</span></span>

### <span data-ttu-id="ef38c-111">Esempio 1 eliminare un IotHub</span><span class="sxs-lookup"><span data-stu-id="ef38c-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="ef38c-112">Rimuove la chiave denominata iothubowner1 dalla IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ef38c-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ef38c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef38c-113">PARAMETERS</span></span>

### <span data-ttu-id="ef38c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef38c-114">-DefaultProfile</span></span>
<span data-ttu-id="ef38c-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ef38c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef38c-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="ef38c-116">-HubId</span></span>
<span data-ttu-id="ef38c-117">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="ef38c-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef38c-118">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ef38c-118">-KeyName</span></span>
<span data-ttu-id="ef38c-119">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="ef38c-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef38c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef38c-120">-Name</span></span>
<span data-ttu-id="ef38c-121">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="ef38c-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef38c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef38c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef38c-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ef38c-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef38c-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ef38c-124">-Confirm</span></span>
<span data-ttu-id="ef38c-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef38c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef38c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef38c-126">-WhatIf</span></span>
<span data-ttu-id="ef38c-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef38c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef38c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef38c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef38c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef38c-129">CommonParameters</span></span>
<span data-ttu-id="ef38c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef38c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef38c-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef38c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef38c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef38c-132">INPUTS</span></span>

### <span data-ttu-id="ef38c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ef38c-133">System.String</span></span>

## <span data-ttu-id="ef38c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef38c-134">OUTPUTS</span></span>

### <span data-ttu-id="ef38c-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ef38c-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="ef38c-136">Note</span><span class="sxs-lookup"><span data-stu-id="ef38c-136">NOTES</span></span>

## <span data-ttu-id="ef38c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef38c-137">RELATED LINKS</span></span>
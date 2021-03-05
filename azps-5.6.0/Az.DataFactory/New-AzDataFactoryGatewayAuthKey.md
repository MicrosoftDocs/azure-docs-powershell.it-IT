---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: e58df40aa227e1c8132902c467c2dbcb881c7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974958"
---
# <span data-ttu-id="41eaa-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="41eaa-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="41eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="41eaa-103">Crea una chiave di autenticazione per un Gateway di Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="41eaa-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="41eaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41eaa-104">SYNTAX</span></span>

### <span data-ttu-id="41eaa-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="41eaa-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41eaa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="41eaa-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41eaa-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41eaa-107">DESCRIPTION</span></span>
<span data-ttu-id="41eaa-108">Il cmdlet **New-AzDataFactoryGatewayAuthKey crea** la chiave di autenticazione del gateway per un gateway di Data factory di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="41eaa-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="41eaa-109">Per registrare il gateway in un servizio cloud, usare questa chiave.</span><span class="sxs-lookup"><span data-stu-id="41eaa-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="41eaa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41eaa-110">EXAMPLES</span></span>

### <span data-ttu-id="41eaa-111">Esempio 1: Crea una chiave di autenticazione del gateway per Key1</span><span class="sxs-lookup"><span data-stu-id="41eaa-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="41eaa-112">Questo comando crea una chiave di autenticazione del gateway di Key1 per il gateway del data factory denominato MyGateway.</span><span class="sxs-lookup"><span data-stu-id="41eaa-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="41eaa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41eaa-113">PARAMETERS</span></span>

### <span data-ttu-id="41eaa-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="41eaa-114">-DataFactoryName</span></span>
<span data-ttu-id="41eaa-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="41eaa-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41eaa-116">-DefaultProfile</span></span>
<span data-ttu-id="41eaa-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="41eaa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41eaa-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="41eaa-118">-GatewayName</span></span>
<span data-ttu-id="41eaa-119">Nome del gateway di data factory.</span><span class="sxs-lookup"><span data-stu-id="41eaa-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="41eaa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41eaa-120">-InputObject</span></span>
<span data-ttu-id="41eaa-121">Oggetto data factory</span><span class="sxs-lookup"><span data-stu-id="41eaa-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="41eaa-122">-KeyName</span></span>
<span data-ttu-id="41eaa-123">Nome della chiave di autenticazione del gateway da rigenerare, "chiave1" o "chiave2".</span><span class="sxs-lookup"><span data-stu-id="41eaa-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41eaa-124">-ResourceGroupName</span></span>
<span data-ttu-id="41eaa-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41eaa-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41eaa-126">-Confirm</span></span>
<span data-ttu-id="41eaa-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41eaa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41eaa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41eaa-128">-WhatIf</span></span>
<span data-ttu-id="41eaa-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41eaa-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41eaa-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41eaa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41eaa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41eaa-131">CommonParameters</span></span>
<span data-ttu-id="41eaa-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41eaa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41eaa-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41eaa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41eaa-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="41eaa-134">INPUTS</span></span>

### <span data-ttu-id="41eaa-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="41eaa-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="41eaa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="41eaa-136">System.String</span></span>

## <span data-ttu-id="41eaa-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41eaa-137">OUTPUTS</span></span>

### <span data-ttu-id="41eaa-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="41eaa-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="41eaa-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="41eaa-139">NOTES</span></span>
* <span data-ttu-id="41eaa-140">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="41eaa-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="41eaa-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41eaa-141">RELATED LINKS</span></span>

<span data-ttu-id="41eaa-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="41eaa-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 569a1c2d19726bb53ede33145e9151cf8ecd6727
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674988"
---
# <span data-ttu-id="37ed7-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="37ed7-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="37ed7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="37ed7-103">Crea la chiave auth per un gateway di Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="37ed7-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="37ed7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37ed7-104">SYNTAX</span></span>

### <span data-ttu-id="37ed7-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37ed7-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37ed7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="37ed7-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37ed7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37ed7-107">DESCRIPTION</span></span>
<span data-ttu-id="37ed7-108">Il cmdlet **New-AzDataFactoryGatewayAuthKey** crea la chiave di autenticazione del gateway per un gateway di Azure Data Factory specificato.</span><span class="sxs-lookup"><span data-stu-id="37ed7-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="37ed7-109">Il gateway viene registrato con un servizio cloud usando questa chiave.</span><span class="sxs-lookup"><span data-stu-id="37ed7-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="37ed7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37ed7-110">EXAMPLES</span></span>

### <span data-ttu-id="37ed7-111">Esempio 1: crea una chiave di autenticazione Gateway per Key1</span><span class="sxs-lookup"><span data-stu-id="37ed7-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="37ed7-112">Questo comando crea una chiave di autenticazione Gateway di key1 per il gateway di data factory denominato gateway.</span><span class="sxs-lookup"><span data-stu-id="37ed7-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="37ed7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37ed7-113">PARAMETERS</span></span>

### <span data-ttu-id="37ed7-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="37ed7-114">-DataFactoryName</span></span>
<span data-ttu-id="37ed7-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="37ed7-115">The data factory name.</span></span>

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

### <span data-ttu-id="37ed7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ed7-116">-DefaultProfile</span></span>
<span data-ttu-id="37ed7-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="37ed7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37ed7-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="37ed7-118">-GatewayName</span></span>
<span data-ttu-id="37ed7-119">Nome del gateway di data factory.</span><span class="sxs-lookup"><span data-stu-id="37ed7-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="37ed7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37ed7-120">-InputObject</span></span>
<span data-ttu-id="37ed7-121">Oggetto Data Factory</span><span class="sxs-lookup"><span data-stu-id="37ed7-121">The data factory object</span></span>

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

### <span data-ttu-id="37ed7-122">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="37ed7-122">-KeyName</span></span>
<span data-ttu-id="37ed7-123">Il nome della chiave di autenticazione del gateway da rigenerare, "Key1" o "key2".</span><span class="sxs-lookup"><span data-stu-id="37ed7-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="37ed7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ed7-124">-ResourceGroupName</span></span>
<span data-ttu-id="37ed7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37ed7-125">The resource group name.</span></span>

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

### <span data-ttu-id="37ed7-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37ed7-126">-Confirm</span></span>
<span data-ttu-id="37ed7-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ed7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ed7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ed7-128">-WhatIf</span></span>
<span data-ttu-id="37ed7-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37ed7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37ed7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37ed7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ed7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ed7-131">CommonParameters</span></span>
<span data-ttu-id="37ed7-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ed7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ed7-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ed7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ed7-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37ed7-134">INPUTS</span></span>

### <span data-ttu-id="37ed7-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="37ed7-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="37ed7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="37ed7-136">System.String</span></span>

## <span data-ttu-id="37ed7-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37ed7-137">OUTPUTS</span></span>

### <span data-ttu-id="37ed7-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="37ed7-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="37ed7-139">Note</span><span class="sxs-lookup"><span data-stu-id="37ed7-139">NOTES</span></span>
* <span data-ttu-id="37ed7-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="37ed7-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="37ed7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37ed7-141">RELATED LINKS</span></span>

<span data-ttu-id="37ed7-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="37ed7-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>


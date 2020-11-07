---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bed116bedbd06919728da8727cad609813bfc2a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677746"
---
# <span data-ttu-id="339cb-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="339cb-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="339cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="339cb-102">SYNOPSIS</span></span>
<span data-ttu-id="339cb-103">Modifica un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="339cb-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="339cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="339cb-104">SYNTAX</span></span>

### <span data-ttu-id="339cb-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="339cb-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="339cb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="339cb-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="339cb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="339cb-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339cb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="339cb-108">DESCRIPTION</span></span>
<span data-ttu-id="339cb-109">Il cmdlet Update-AzPowerBIEmbeddedCapacity modifica un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="339cb-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="339cb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="339cb-110">EXAMPLES</span></span>

### <span data-ttu-id="339cb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="339cb-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="339cb-112">Modifica la capacità denominata testcapacity in ResourceGroup TestGroup per impostare i contrassegni come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="339cb-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="339cb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="339cb-113">PARAMETERS</span></span>

### <span data-ttu-id="339cb-114">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="339cb-114">-Administrator</span></span>
<span data-ttu-id="339cb-115">Nomi di capacità separati da virgola da impostare come amministratore per la capacità</span><span class="sxs-lookup"><span data-stu-id="339cb-115">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339cb-116">-DefaultProfile</span></span>
<span data-ttu-id="339cb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="339cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339cb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="339cb-118">-InputObject</span></span>
<span data-ttu-id="339cb-119">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="339cb-119">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="339cb-120">-Name</span></span>
<span data-ttu-id="339cb-121">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="339cb-121">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="339cb-122">-PassThru</span></span>
<span data-ttu-id="339cb-123">Restituirà i dettagli della capacità eliminata se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="339cb-123">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="339cb-125">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="339cb-125">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="339cb-126">-ResourceId</span></span>
<span data-ttu-id="339cb-127">PowerBI capacità incorporata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="339cb-127">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="339cb-128">-Sku</span></span>
<span data-ttu-id="339cb-129">Nome dell'USK per la capacità.</span><span class="sxs-lookup"><span data-stu-id="339cb-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="339cb-130">-Tag</span></span>
<span data-ttu-id="339cb-131">Coppie chiave-valore nella forma di una tabella hash impostata come tag sulla capacità.</span><span class="sxs-lookup"><span data-stu-id="339cb-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339cb-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="339cb-132">-Confirm</span></span>
<span data-ttu-id="339cb-133">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="339cb-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="339cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339cb-134">-WhatIf</span></span>
<span data-ttu-id="339cb-135">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="339cb-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="339cb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339cb-136">CommonParameters</span></span>
<span data-ttu-id="339cb-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339cb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339cb-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339cb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339cb-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="339cb-139">INPUTS</span></span>

### <span data-ttu-id="339cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="339cb-140">System.String</span></span>

### <span data-ttu-id="339cb-141">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="339cb-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="339cb-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="339cb-142">OUTPUTS</span></span>

### <span data-ttu-id="339cb-143">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="339cb-143">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="339cb-144">Note</span><span class="sxs-lookup"><span data-stu-id="339cb-144">NOTES</span></span>

## <span data-ttu-id="339cb-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="339cb-145">RELATED LINKS</span></span>

[<span data-ttu-id="339cb-146">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="339cb-146">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="339cb-147">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="339cb-147">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)

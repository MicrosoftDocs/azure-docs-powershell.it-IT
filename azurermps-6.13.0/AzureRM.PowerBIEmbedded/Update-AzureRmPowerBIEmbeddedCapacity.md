---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520891"
---
# <span data-ttu-id="a8fd6-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a8fd6-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a8fd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fd6-103">Modifica un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a8fd6-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8fd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8fd6-104">SYNTAX</span></span>

### <span data-ttu-id="a8fd6-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8fd6-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8fd6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8fd6-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8fd6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a8fd6-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8fd6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8fd6-108">DESCRIPTION</span></span>
<span data-ttu-id="a8fd6-109">Il cmdlet Update-AzureRmPowerBIEmbeddedCapacity modifica un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="a8fd6-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a8fd6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8fd6-110">EXAMPLES</span></span>

### <span data-ttu-id="a8fd6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8fd6-111">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
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

<span data-ttu-id="a8fd6-112">Modifica la capacità denominata testcapacity in ResourceGroup TestGroup per impostare i contrassegni come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="a8fd6-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="a8fd6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8fd6-113">PARAMETERS</span></span>

### <span data-ttu-id="a8fd6-114">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="a8fd6-114">-Administrator</span></span>
<span data-ttu-id="a8fd6-115">Nomi di capacità separati da virgola da impostare come amministratore per la capacità</span><span class="sxs-lookup"><span data-stu-id="a8fd6-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="a8fd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8fd6-116">-DefaultProfile</span></span>
<span data-ttu-id="a8fd6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8fd6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8fd6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8fd6-118">-InputObject</span></span>
<span data-ttu-id="a8fd6-119">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="a8fd6-119">Input object for Piping</span></span>

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

### <span data-ttu-id="a8fd6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8fd6-120">-Name</span></span>
<span data-ttu-id="a8fd6-121">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="a8fd6-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="a8fd6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8fd6-122">-PassThru</span></span>
<span data-ttu-id="a8fd6-123">Restituirà i dettagli della capacità eliminata se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="a8fd6-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="a8fd6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8fd6-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8fd6-125">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="a8fd6-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="a8fd6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8fd6-126">-ResourceId</span></span>
<span data-ttu-id="a8fd6-127">PowerBI capacità incorporata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a8fd6-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="a8fd6-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="a8fd6-128">-Sku</span></span>
<span data-ttu-id="a8fd6-129">Nome dell'USK per la capacità.</span><span class="sxs-lookup"><span data-stu-id="a8fd6-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="a8fd6-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8fd6-130">-Tag</span></span>
<span data-ttu-id="a8fd6-131">Coppie chiave-valore nella forma di una tabella hash impostata come tag sulla capacità.</span><span class="sxs-lookup"><span data-stu-id="a8fd6-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="a8fd6-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8fd6-132">-Confirm</span></span>
<span data-ttu-id="a8fd6-133">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="a8fd6-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a8fd6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8fd6-134">-WhatIf</span></span>
<span data-ttu-id="a8fd6-135">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="a8fd6-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a8fd6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fd6-136">CommonParameters</span></span>
<span data-ttu-id="a8fd6-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8fd6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fd6-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8fd6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fd6-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8fd6-139">INPUTS</span></span>

### <span data-ttu-id="a8fd6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a8fd6-140">System.String</span></span>

### <span data-ttu-id="a8fd6-141">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a8fd6-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="a8fd6-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8fd6-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a8fd6-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8fd6-143">OUTPUTS</span></span>

### <span data-ttu-id="a8fd6-144">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a8fd6-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a8fd6-145">Note</span><span class="sxs-lookup"><span data-stu-id="a8fd6-145">NOTES</span></span>

## <span data-ttu-id="a8fd6-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8fd6-146">RELATED LINKS</span></span>

[<span data-ttu-id="a8fd6-147">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a8fd6-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a8fd6-148">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a8fd6-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)

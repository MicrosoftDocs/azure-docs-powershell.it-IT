---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508080"
---
# <span data-ttu-id="64b15-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64b15-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="64b15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64b15-102">SYNOPSIS</span></span>
<span data-ttu-id="64b15-103">Modifica un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="64b15-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64b15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64b15-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="64b15-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64b15-105">DESCRIPTION</span></span>
<span data-ttu-id="64b15-106">Il cmdlet Update-AzureRmPowerBIEmbeddedCapacity modifica un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="64b15-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="64b15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64b15-107">EXAMPLES</span></span>

### <span data-ttu-id="64b15-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64b15-108">Example 1</span></span>
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

<span data-ttu-id="64b15-109">Modifica la capacità denominata testcapacity in ResourceGroup TestGroup per impostare i contrassegni come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="64b15-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="64b15-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64b15-110">PARAMETERS</span></span>

### <span data-ttu-id="64b15-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="64b15-111">-Name</span></span>
<span data-ttu-id="64b15-112">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="64b15-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="64b15-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b15-113">-ResourceGroupName</span></span>
<span data-ttu-id="64b15-114">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="64b15-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="64b15-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="64b15-115">-Sku</span></span>
<span data-ttu-id="64b15-116">Nome dell'USK per la capacità.</span><span class="sxs-lookup"><span data-stu-id="64b15-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="64b15-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="64b15-117">-Tag</span></span>
<span data-ttu-id="64b15-118">Coppie chiave-valore nella forma di una tabella hash impostata come tag sulla capacità.</span><span class="sxs-lookup"><span data-stu-id="64b15-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="64b15-119">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="64b15-119">-Administrator</span></span>
<span data-ttu-id="64b15-120">Nomi di capacità separati da virgola da impostare come amministratore per la capacità</span><span class="sxs-lookup"><span data-stu-id="64b15-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="64b15-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64b15-121">-ResourceId</span></span>
<span data-ttu-id="64b15-122">PowerBI capacità incorporata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="64b15-122">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b15-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64b15-123">-InputObject</span></span>
<span data-ttu-id="64b15-124">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="64b15-124">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b15-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64b15-125">-PassThru</span></span>
<span data-ttu-id="64b15-126">Restituirà i dettagli della capacità eliminata se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="64b15-126">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b15-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64b15-127">-Confirm</span></span>
<span data-ttu-id="64b15-128">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="64b15-128">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="64b15-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b15-129">-WhatIf</span></span>
<span data-ttu-id="64b15-130">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="64b15-130">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="64b15-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b15-131">CommonParameters</span></span>
<span data-ttu-id="64b15-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b15-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b15-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b15-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b15-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64b15-134">INPUTS</span></span>

### <span data-ttu-id="64b15-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="64b15-135">None</span></span>
<span data-ttu-id="64b15-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="64b15-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64b15-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64b15-137">OUTPUTS</span></span>

### <span data-ttu-id="64b15-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64b15-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="64b15-139">Note</span><span class="sxs-lookup"><span data-stu-id="64b15-139">NOTES</span></span>

## <span data-ttu-id="64b15-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64b15-140">RELATED LINKS</span></span>

[<span data-ttu-id="64b15-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64b15-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="64b15-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="64b15-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022427"
---
# <span data-ttu-id="4136c-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4136c-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4136c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4136c-102">SYNOPSIS</span></span>
<span data-ttu-id="4136c-103">Modifica un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="4136c-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4136c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4136c-104">SYNTAX</span></span>

### <span data-ttu-id="4136c-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4136c-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4136c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4136c-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4136c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4136c-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4136c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4136c-108">DESCRIPTION</span></span>
<span data-ttu-id="4136c-109">Il cmdlet Update-AzPowerBIEmbeddedCapacity modifica un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="4136c-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4136c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4136c-110">EXAMPLES</span></span>

### <span data-ttu-id="4136c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4136c-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="4136c-112">Modifica la capacità denominata testcapacity in ResourceGroup TestGroup per impostare i tag come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com testuser2@contoso.com e l'entità del servizio: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="4136c-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="4136c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4136c-113">PARAMETERS</span></span>

### <span data-ttu-id="4136c-114">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="4136c-114">-Administrator</span></span>
<span data-ttu-id="4136c-115">Nomi separati da virgola da impostare come amministratori per la capacità.</span><span class="sxs-lookup"><span data-stu-id="4136c-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="4136c-116">Per Service Principal: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="4136c-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="4136c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4136c-117">-DefaultProfile</span></span>
<span data-ttu-id="4136c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4136c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4136c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4136c-119">-InputObject</span></span>
<span data-ttu-id="4136c-120">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="4136c-120">Input object for Piping</span></span>

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

### <span data-ttu-id="4136c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4136c-121">-Name</span></span>
<span data-ttu-id="4136c-122">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="4136c-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="4136c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4136c-123">-PassThru</span></span>
<span data-ttu-id="4136c-124">Restituirà i dettagli della capacità eliminata se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="4136c-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="4136c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4136c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4136c-126">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="4136c-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="4136c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4136c-127">-ResourceId</span></span>
<span data-ttu-id="4136c-128">PowerBI capacità incorporata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="4136c-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="4136c-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="4136c-129">-Sku</span></span>
<span data-ttu-id="4136c-130">Nome dell'USK per la capacità.</span><span class="sxs-lookup"><span data-stu-id="4136c-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="4136c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4136c-131">-Tag</span></span>
<span data-ttu-id="4136c-132">Coppie chiave-valore nella forma di una tabella hash impostata come tag sulla capacità.</span><span class="sxs-lookup"><span data-stu-id="4136c-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="4136c-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4136c-133">-Confirm</span></span>
<span data-ttu-id="4136c-134">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="4136c-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4136c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4136c-135">-WhatIf</span></span>
<span data-ttu-id="4136c-136">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="4136c-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4136c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4136c-137">CommonParameters</span></span>
<span data-ttu-id="4136c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4136c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4136c-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4136c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4136c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4136c-140">INPUTS</span></span>

### <span data-ttu-id="4136c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4136c-141">System.String</span></span>

### <span data-ttu-id="4136c-142">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4136c-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4136c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4136c-143">OUTPUTS</span></span>

### <span data-ttu-id="4136c-144">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4136c-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4136c-145">Note</span><span class="sxs-lookup"><span data-stu-id="4136c-145">NOTES</span></span>

## <span data-ttu-id="4136c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4136c-146">RELATED LINKS</span></span>

[<span data-ttu-id="4136c-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4136c-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4136c-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4136c-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)

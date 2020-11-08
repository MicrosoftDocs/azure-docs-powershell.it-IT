---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031821"
---
# <span data-ttu-id="44a30-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="44a30-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="44a30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44a30-102">SYNOPSIS</span></span>
<span data-ttu-id="44a30-103">Crea un nuovo ordine per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44a30-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="44a30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44a30-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44a30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44a30-105">DESCRIPTION</span></span>
<span data-ttu-id="44a30-106">Il cmdlet **New-AzDataBoxEdgeOrder** crea un nuovo ordine per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="44a30-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="44a30-107">Prima di creare un ordine, è necessario creare una risorsa per il dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="44a30-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="44a30-108">Puoi specificare i dettagli come i parametri di contatto, nome società, posta elettronica, indirizzo e così via come per la creazione dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="44a30-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="44a30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44a30-109">EXAMPLES</span></span>

### <span data-ttu-id="44a30-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44a30-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="44a30-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44a30-111">PARAMETERS</span></span>

### <span data-ttu-id="44a30-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="44a30-112">-AddressLine1</span></span>
<span data-ttu-id="44a30-113">Indirizzo prima riga</span><span class="sxs-lookup"><span data-stu-id="44a30-113">Address first line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="44a30-114">-AddressLine2</span></span>
<span data-ttu-id="44a30-115">Indirizzo della seconda riga</span><span class="sxs-lookup"><span data-stu-id="44a30-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="44a30-116">-AddressLine3</span></span>
<span data-ttu-id="44a30-117">Indirizzo terza riga</span><span class="sxs-lookup"><span data-stu-id="44a30-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44a30-118">-AsJob</span></span>
<span data-ttu-id="44a30-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44a30-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44a30-120">-Città</span><span class="sxs-lookup"><span data-stu-id="44a30-120">-City</span></span>
<span data-ttu-id="44a30-121">Nome della città</span><span class="sxs-lookup"><span data-stu-id="44a30-121">Name of the City</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="44a30-122">-CompanyName</span></span>
<span data-ttu-id="44a30-123">Nome della società</span><span class="sxs-lookup"><span data-stu-id="44a30-123">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="44a30-124">-ContactPerson</span></span>
<span data-ttu-id="44a30-125">Nome della persona di contatto</span><span class="sxs-lookup"><span data-stu-id="44a30-125">Name of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-126">-Paese</span><span class="sxs-lookup"><span data-stu-id="44a30-126">-Country</span></span>
<span data-ttu-id="44a30-127">Nome del paese</span><span class="sxs-lookup"><span data-stu-id="44a30-127">Name of the Country</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a30-128">-DefaultProfile</span></span>
<span data-ttu-id="44a30-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44a30-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44a30-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="44a30-130">-DeviceName</span></span>
<span data-ttu-id="44a30-131">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="44a30-131">Resource Name</span></span>

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

### <span data-ttu-id="44a30-132">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="44a30-132">-Email</span></span>
<span data-ttu-id="44a30-133">Elenco dei messaggi di posta elettronica per ricevere gli aggiornamenti, accetta massimo di 10 messaggi di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="44a30-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-134">-Telefono</span><span class="sxs-lookup"><span data-stu-id="44a30-134">-Phone</span></span>
<span data-ttu-id="44a30-135">Numero di telefono della persona di contatto</span><span class="sxs-lookup"><span data-stu-id="44a30-135">Phone number of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-136">-Cap</span><span class="sxs-lookup"><span data-stu-id="44a30-136">-PostalCode</span></span>
<span data-ttu-id="44a30-137">Codice postale dell'indirizzo</span><span class="sxs-lookup"><span data-stu-id="44a30-137">Postal Code of the Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a30-138">-ResourceGroupName</span></span>
<span data-ttu-id="44a30-139">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="44a30-139">Resource Group Name</span></span>

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

### <span data-ttu-id="44a30-140">-Stato</span><span class="sxs-lookup"><span data-stu-id="44a30-140">-State</span></span>
<span data-ttu-id="44a30-141">Nome dello stato</span><span class="sxs-lookup"><span data-stu-id="44a30-141">Name of the State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a30-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44a30-142">-Confirm</span></span>
<span data-ttu-id="44a30-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44a30-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44a30-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44a30-144">-WhatIf</span></span>
<span data-ttu-id="44a30-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44a30-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44a30-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44a30-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44a30-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a30-147">CommonParameters</span></span>
<span data-ttu-id="44a30-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a30-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a30-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44a30-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a30-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44a30-150">INPUTS</span></span>

### <span data-ttu-id="44a30-151">System. String</span><span class="sxs-lookup"><span data-stu-id="44a30-151">System.String</span></span>

## <span data-ttu-id="44a30-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44a30-152">OUTPUTS</span></span>

### <span data-ttu-id="44a30-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="44a30-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="44a30-154">Note</span><span class="sxs-lookup"><span data-stu-id="44a30-154">NOTES</span></span>

## <span data-ttu-id="44a30-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44a30-155">RELATED LINKS</span></span>

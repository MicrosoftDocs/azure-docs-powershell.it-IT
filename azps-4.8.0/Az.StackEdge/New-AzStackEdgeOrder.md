---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191175"
---
# <span data-ttu-id="26fee-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="26fee-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="26fee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26fee-102">SYNOPSIS</span></span>
<span data-ttu-id="26fee-103">Crea un nuovo ordine per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26fee-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="26fee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26fee-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26fee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26fee-105">DESCRIPTION</span></span>
<span data-ttu-id="26fee-106">Il cmdlet **New-AzStackEdgeOrder** crea un nuovo ordine per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="26fee-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="26fee-107">Prima di creare un ordine, è necessario creare una risorsa per il dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="26fee-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="26fee-108">Puoi specificare i dettagli come i parametri di contatto, nome società, posta elettronica, indirizzo e così via come per la creazione dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="26fee-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="26fee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26fee-109">EXAMPLES</span></span>

### <span data-ttu-id="26fee-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26fee-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="26fee-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26fee-111">PARAMETERS</span></span>

### <span data-ttu-id="26fee-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="26fee-112">-AddressLine1</span></span>
<span data-ttu-id="26fee-113">Indirizzo prima riga</span><span class="sxs-lookup"><span data-stu-id="26fee-113">Address first line</span></span>

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

### <span data-ttu-id="26fee-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="26fee-114">-AddressLine2</span></span>
<span data-ttu-id="26fee-115">Indirizzo della seconda riga</span><span class="sxs-lookup"><span data-stu-id="26fee-115">Address second line</span></span>

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

### <span data-ttu-id="26fee-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="26fee-116">-AddressLine3</span></span>
<span data-ttu-id="26fee-117">Indirizzo terza riga</span><span class="sxs-lookup"><span data-stu-id="26fee-117">Address third line</span></span>

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

### <span data-ttu-id="26fee-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26fee-118">-AsJob</span></span>
<span data-ttu-id="26fee-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="26fee-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26fee-120">-Città</span><span class="sxs-lookup"><span data-stu-id="26fee-120">-City</span></span>
<span data-ttu-id="26fee-121">Nome della città</span><span class="sxs-lookup"><span data-stu-id="26fee-121">Name of the City</span></span>

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

### <span data-ttu-id="26fee-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="26fee-122">-CompanyName</span></span>
<span data-ttu-id="26fee-123">Nome della società</span><span class="sxs-lookup"><span data-stu-id="26fee-123">Name of the company</span></span>

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

### <span data-ttu-id="26fee-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="26fee-124">-ContactPerson</span></span>
<span data-ttu-id="26fee-125">Nome della persona di contatto</span><span class="sxs-lookup"><span data-stu-id="26fee-125">Name of the contact person</span></span>

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

### <span data-ttu-id="26fee-126">-Paese</span><span class="sxs-lookup"><span data-stu-id="26fee-126">-Country</span></span>
<span data-ttu-id="26fee-127">Nome del paese</span><span class="sxs-lookup"><span data-stu-id="26fee-127">Name of the Country</span></span>

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

### <span data-ttu-id="26fee-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fee-128">-DefaultProfile</span></span>
<span data-ttu-id="26fee-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26fee-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26fee-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="26fee-130">-DeviceName</span></span>
<span data-ttu-id="26fee-131">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="26fee-131">Resource Name</span></span>

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

### <span data-ttu-id="26fee-132">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="26fee-132">-Email</span></span>
<span data-ttu-id="26fee-133">Elenco dei messaggi di posta elettronica per ricevere gli aggiornamenti, accetta massimo di 10 messaggi di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="26fee-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="26fee-134">-Telefono</span><span class="sxs-lookup"><span data-stu-id="26fee-134">-Phone</span></span>
<span data-ttu-id="26fee-135">Numero di telefono della persona di contatto</span><span class="sxs-lookup"><span data-stu-id="26fee-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="26fee-136">-Cap</span><span class="sxs-lookup"><span data-stu-id="26fee-136">-PostalCode</span></span>
<span data-ttu-id="26fee-137">Codice postale dell'indirizzo</span><span class="sxs-lookup"><span data-stu-id="26fee-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="26fee-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26fee-138">-ResourceGroupName</span></span>
<span data-ttu-id="26fee-139">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="26fee-139">Resource Group Name</span></span>

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

### <span data-ttu-id="26fee-140">-Stato</span><span class="sxs-lookup"><span data-stu-id="26fee-140">-State</span></span>
<span data-ttu-id="26fee-141">Nome dello stato</span><span class="sxs-lookup"><span data-stu-id="26fee-141">Name of the State</span></span>

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

### <span data-ttu-id="26fee-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26fee-142">-Confirm</span></span>
<span data-ttu-id="26fee-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26fee-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26fee-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26fee-144">-WhatIf</span></span>
<span data-ttu-id="26fee-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26fee-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26fee-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26fee-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26fee-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fee-147">CommonParameters</span></span>
<span data-ttu-id="26fee-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26fee-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fee-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26fee-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fee-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26fee-150">INPUTS</span></span>

### <span data-ttu-id="26fee-151">System. String</span><span class="sxs-lookup"><span data-stu-id="26fee-151">System.String</span></span>

## <span data-ttu-id="26fee-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26fee-152">OUTPUTS</span></span>

### <span data-ttu-id="26fee-153">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="26fee-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="26fee-154">Note</span><span class="sxs-lookup"><span data-stu-id="26fee-154">NOTES</span></span>

## <span data-ttu-id="26fee-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26fee-155">RELATED LINKS</span></span>

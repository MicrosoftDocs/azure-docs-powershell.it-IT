---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474089"
---
# <span data-ttu-id="bc018-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="bc018-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="bc018-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc018-102">SYNOPSIS</span></span>
<span data-ttu-id="bc018-103">Modifica una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="bc018-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc018-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc018-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc018-105">DESCRIPTION</span></span>
<span data-ttu-id="bc018-106">Il cmdlet **set-AzIntegrationAccountMap** modifica una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="bc018-107">Questo cmdlet restituisce un oggetto che rappresenta la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="bc018-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="bc018-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="bc018-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="bc018-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bc018-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="bc018-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bc018-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="bc018-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bc018-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="bc018-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bc018-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc018-113">EXAMPLES</span></span>

### <span data-ttu-id="bc018-114">Esempio 1: modificare una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="bc018-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="bc018-115">Questo comando modifica la mappa dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="bc018-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="bc018-116">Il comando specifica una definizione di mappa archiviata nella variabile $MapContent da un comando precedente.</span><span class="sxs-lookup"><span data-stu-id="bc018-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="bc018-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bc018-117">Example 2</span></span>

<span data-ttu-id="bc018-118">Modifica una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-118">Modifies an integration account map.</span></span> <span data-ttu-id="bc018-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="bc018-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="bc018-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc018-120">PARAMETERS</span></span>

### <span data-ttu-id="bc018-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="bc018-121">-ContentType</span></span>
<span data-ttu-id="bc018-122">Specifica un tipo di contenuto per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="bc018-123">Questo cmdlet supporta Application/XML come tipo di contenuto map.</span><span class="sxs-lookup"><span data-stu-id="bc018-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="bc018-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc018-124">-DefaultProfile</span></span>
<span data-ttu-id="bc018-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bc018-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc018-126">-Force</span><span class="sxs-lookup"><span data-stu-id="bc018-126">-Force</span></span>
<span data-ttu-id="bc018-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc018-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc018-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="bc018-128">-MapDefinition</span></span>
<span data-ttu-id="bc018-129">Specifica un oggetto Definition per la mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="bc018-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="bc018-130">-MapFilePath</span></span>
<span data-ttu-id="bc018-131">Specifica il percorso del file di una definizione per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="bc018-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="bc018-132">-MapName</span></span>
<span data-ttu-id="bc018-133">Specifica il nome di una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-133">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc018-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="bc018-134">-MapType</span></span>
<span data-ttu-id="bc018-135">Specifica il tipo per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="bc018-136">Questo cmdlet supporta l'XSLT come tipo di mappa.</span><span class="sxs-lookup"><span data-stu-id="bc018-136">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc018-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="bc018-137">-Metadata</span></span>
<span data-ttu-id="bc018-138">Specifica un oggetto Metadata per la mappa.</span><span class="sxs-lookup"><span data-stu-id="bc018-138">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc018-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc018-139">-Name</span></span>
<span data-ttu-id="bc018-140">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="bc018-140">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc018-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc018-141">-ResourceGroupName</span></span>
<span data-ttu-id="bc018-142">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc018-142">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc018-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc018-143">-Confirm</span></span>
<span data-ttu-id="bc018-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc018-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc018-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc018-145">-WhatIf</span></span>
<span data-ttu-id="bc018-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc018-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc018-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc018-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc018-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc018-148">CommonParameters</span></span>
<span data-ttu-id="bc018-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc018-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc018-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc018-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc018-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc018-151">INPUTS</span></span>

### <span data-ttu-id="bc018-152">System. String</span><span class="sxs-lookup"><span data-stu-id="bc018-152">System.String</span></span>

## <span data-ttu-id="bc018-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc018-153">OUTPUTS</span></span>

### <span data-ttu-id="bc018-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="bc018-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="bc018-155">Note</span><span class="sxs-lookup"><span data-stu-id="bc018-155">NOTES</span></span>

## <span data-ttu-id="bc018-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc018-156">RELATED LINKS</span></span>

[<span data-ttu-id="bc018-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="bc018-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="bc018-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="bc018-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="bc018-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="bc018-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)



---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 3e4a8a68ce6af6a8be30750d0eaf8e5393ac409f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687170"
---
# <span data-ttu-id="beb95-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="beb95-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="beb95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="beb95-102">SYNOPSIS</span></span>
<span data-ttu-id="beb95-103">Modifica una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beb95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="beb95-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="beb95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beb95-105">DESCRIPTION</span></span>
<span data-ttu-id="beb95-106">Il cmdlet **set-AzureRmIntegrationAccountMap** modifica una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="beb95-107">Questo cmdlet restituisce un oggetto che rappresenta la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="beb95-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="beb95-108">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="beb95-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="beb95-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="beb95-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="beb95-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="beb95-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="beb95-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="beb95-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="beb95-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="beb95-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="beb95-113">EXAMPLES</span></span>

### <span data-ttu-id="beb95-114">Esempio 1: modificare una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="beb95-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="beb95-115">Questo comando modifica la mappa dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="beb95-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="beb95-116">Il comando specifica una definizione di mappa archiviata nella variabile $MapContent da un comando precedente.</span><span class="sxs-lookup"><span data-stu-id="beb95-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="beb95-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="beb95-117">PARAMETERS</span></span>

### <span data-ttu-id="beb95-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="beb95-118">-ContentType</span></span>
<span data-ttu-id="beb95-119">Specifica un tipo di contenuto per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="beb95-120">Questo cmdlet supporta Application/XML come tipo di contenuto map.</span><span class="sxs-lookup"><span data-stu-id="beb95-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="beb95-121">-Force</span><span class="sxs-lookup"><span data-stu-id="beb95-121">-Force</span></span>
<span data-ttu-id="beb95-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="beb95-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="beb95-123">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="beb95-123">-MapDefinition</span></span>
<span data-ttu-id="beb95-124">Specifica un oggetto Definition per la mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-124">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="beb95-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="beb95-125">-MapFilePath</span></span>
<span data-ttu-id="beb95-126">Specifica il percorso del file di una definizione per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-126">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="beb95-127">-MapName</span><span class="sxs-lookup"><span data-stu-id="beb95-127">-MapName</span></span>
<span data-ttu-id="beb95-128">Specifica il nome di una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-128">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="beb95-129">-MapType</span><span class="sxs-lookup"><span data-stu-id="beb95-129">-MapType</span></span>
<span data-ttu-id="beb95-130">Specifica il tipo per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-130">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="beb95-131">Questo cmdlet supporta l'XSLT come tipo di mappa.</span><span class="sxs-lookup"><span data-stu-id="beb95-131">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb95-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="beb95-132">-Metadata</span></span>
<span data-ttu-id="beb95-133">Specifica un oggetto Metadata per la mappa.</span><span class="sxs-lookup"><span data-stu-id="beb95-133">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="beb95-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="beb95-134">-Name</span></span>
<span data-ttu-id="beb95-135">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="beb95-135">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="beb95-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beb95-136">-ResourceGroupName</span></span>
<span data-ttu-id="beb95-137">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="beb95-137">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="beb95-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="beb95-138">-Confirm</span></span>
<span data-ttu-id="beb95-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beb95-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beb95-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beb95-140">-WhatIf</span></span>
<span data-ttu-id="beb95-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beb95-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beb95-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beb95-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beb95-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beb95-143">-DefaultProfile</span></span>
<span data-ttu-id="beb95-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="beb95-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beb95-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb95-145">CommonParameters</span></span>
<span data-ttu-id="beb95-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beb95-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb95-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb95-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb95-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="beb95-148">INPUTS</span></span>

## <span data-ttu-id="beb95-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="beb95-149">OUTPUTS</span></span>

### <span data-ttu-id="beb95-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="beb95-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="beb95-151">Note</span><span class="sxs-lookup"><span data-stu-id="beb95-151">NOTES</span></span>

## <span data-ttu-id="beb95-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="beb95-152">RELATED LINKS</span></span>

[<span data-ttu-id="beb95-153">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="beb95-153">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="beb95-154">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="beb95-154">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="beb95-155">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="beb95-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)



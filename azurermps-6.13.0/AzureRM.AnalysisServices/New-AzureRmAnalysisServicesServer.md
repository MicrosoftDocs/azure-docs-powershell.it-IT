---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: d8a795cc27a09fe7b23ac2156115d7a52212e3ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517728"
---
# <span data-ttu-id="a795e-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a795e-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="a795e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a795e-102">SYNOPSIS</span></span>
<span data-ttu-id="a795e-103">Crea un nuovo server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a795e-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a795e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a795e-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a795e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a795e-105">DESCRIPTION</span></span>
<span data-ttu-id="a795e-106">Il cmdlet New-AzureRmAnalysisServicesServer crea un nuovo server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a795e-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="a795e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a795e-107">EXAMPLES</span></span>

### <span data-ttu-id="a795e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a795e-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="a795e-109">Crea un server denominato TestServer in Azure Region West-US e nel gruppo di risorse testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="a795e-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="a795e-110">Il livello SKU per il server sarà S1.</span><span class="sxs-lookup"><span data-stu-id="a795e-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="a795e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a795e-111">PARAMETERS</span></span>

### <span data-ttu-id="a795e-112">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="a795e-112">-Administrator</span></span>
<span data-ttu-id="a795e-113">Stringa che rappresenta un elenco delimitato da virgole di utenti o gruppi da impostare come amministratori nel server.</span><span class="sxs-lookup"><span data-stu-id="a795e-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="a795e-114">Gli utenti o i gruppi devono essere specificati come formato user@contoso.com UPN, ad esempio groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="a795e-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a795e-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="a795e-116">URI del contenitore BLOB per il backup del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a795e-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="a795e-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="a795e-118">Modalità di connessione predefinita di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="a795e-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a795e-119">-DefaultProfile</span></span>
<span data-ttu-id="a795e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a795e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a795e-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="a795e-121">-FirewallConfig</span></span>
<span data-ttu-id="a795e-122">Configurazione del firewall di un server di analisi</span><span class="sxs-lookup"><span data-stu-id="a795e-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a795e-123">-GatewayResourceId</span></span>
<span data-ttu-id="a795e-124">ID risorsa gateway per assocaite in un server di analisi</span><span class="sxs-lookup"><span data-stu-id="a795e-124">Gateway resource Id for assocaite to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a795e-125">-Location</span></span>
<span data-ttu-id="a795e-126">Area di Azure in cui è ospitato il server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a795e-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="a795e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a795e-127">-Name</span></span>
<span data-ttu-id="a795e-128">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a795e-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="a795e-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="a795e-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="a795e-130">Conteggio delle riproduzioni di sola lettura di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="a795e-130">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a795e-131">-ResourceGroupName</span></span>
<span data-ttu-id="a795e-132">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="a795e-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="a795e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a795e-133">-Sku</span></span>
<span data-ttu-id="a795e-134">Nome dell'USK per il server.</span><span class="sxs-lookup"><span data-stu-id="a795e-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="a795e-135">I valori supportati sono 0',' s 1',' s 2',' s 4' per il livello standard; ' B1',' B2' per il livello di base è da 1' per il livello di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="a795e-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="a795e-136">-Tag</span></span>
<span data-ttu-id="a795e-137">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="a795e-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a795e-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a795e-138">-Confirm</span></span>
<span data-ttu-id="a795e-139">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="a795e-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a795e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a795e-140">-WhatIf</span></span>
<span data-ttu-id="a795e-141">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="a795e-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a795e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a795e-142">CommonParameters</span></span>
<span data-ttu-id="a795e-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a795e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a795e-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a795e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a795e-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a795e-145">INPUTS</span></span>

### <span data-ttu-id="a795e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a795e-146">System.String</span></span>

### <span data-ttu-id="a795e-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a795e-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a795e-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a795e-148">System.Int32</span></span>

### <span data-ttu-id="a795e-149">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="a795e-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="a795e-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a795e-150">OUTPUTS</span></span>

### <span data-ttu-id="a795e-151">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a795e-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="a795e-152">Note</span><span class="sxs-lookup"><span data-stu-id="a795e-152">NOTES</span></span>
<span data-ttu-id="a795e-153">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="a795e-153">Alias: New-AzureAs</span></span>

## <span data-ttu-id="a795e-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a795e-154">RELATED LINKS</span></span>

[<span data-ttu-id="a795e-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a795e-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="a795e-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="a795e-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)

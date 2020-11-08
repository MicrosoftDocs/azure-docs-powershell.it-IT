---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: a3c3338db7fb749b3eb4d5e92c438deda0742a67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199938"
---
# <span data-ttu-id="5eedd-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5eedd-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="5eedd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5eedd-102">SYNOPSIS</span></span>
<span data-ttu-id="5eedd-103">Modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="5eedd-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="5eedd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5eedd-104">SYNTAX</span></span>

### <span data-ttu-id="5eedd-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5eedd-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eedd-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="5eedd-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eedd-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="5eedd-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eedd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eedd-108">DESCRIPTION</span></span>
<span data-ttu-id="5eedd-109">Il cmdlet Set-AzAnalysisServicesServer modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="5eedd-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="5eedd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5eedd-110">EXAMPLES</span></span>

### <span data-ttu-id="5eedd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5eedd-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="5eedd-112">Modifica il server denominato TestServer in ResourceGroup TestGroup per impostare i tag come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="5eedd-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="5eedd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5eedd-113">PARAMETERS</span></span>

### <span data-ttu-id="5eedd-114">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="5eedd-114">-Administrator</span></span>
<span data-ttu-id="5eedd-115">Stringa che rappresenta un elenco delimitato da virgole di utenti o gruppi da impostare come amministratori nel server.</span><span class="sxs-lookup"><span data-stu-id="5eedd-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="5eedd-116">Gli utenti o i gruppi devono essere specificati come formato user@contoso.com UPN, ad esempio groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="5eedd-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="5eedd-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="5eedd-118">URI del contenitore BLOB per il backup del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5eedd-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="5eedd-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="5eedd-120">Modalità di connessione predefinita di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="5eedd-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="5eedd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eedd-121">-DefaultProfile</span></span>
<span data-ttu-id="5eedd-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5eedd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eedd-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="5eedd-123">-DisableBackup</span></span>
<span data-ttu-id="5eedd-124">Il passaggio per disabilitare il contenitore di BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="5eedd-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="5eedd-125">Per riattivare il contenitore di BLOB di backup, fornisci l'URI del contenitore BLOB di backup come-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="5eedd-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="5eedd-126">-DisassociateGateway</span></span>
<span data-ttu-id="5eedd-127">Dissocia risorsa gateway da un server di analisi</span><span class="sxs-lookup"><span data-stu-id="5eedd-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="5eedd-128">-FirewallConfig</span></span>
<span data-ttu-id="5eedd-129">Configurazione del firewall di un server di analisi</span><span class="sxs-lookup"><span data-stu-id="5eedd-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="5eedd-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5eedd-130">-GatewayResourceId</span></span>
<span data-ttu-id="5eedd-131">ID risorsa gateway da associare a un server di analisi</span><span class="sxs-lookup"><span data-stu-id="5eedd-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="5eedd-132">-Name</span></span>
<span data-ttu-id="5eedd-133">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5eedd-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="5eedd-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5eedd-134">-PassThru</span></span>
<span data-ttu-id="5eedd-135">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="5eedd-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="5eedd-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5eedd-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="5eedd-137">Conteggio delle riproduzioni di sola lettura di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="5eedd-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="5eedd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eedd-138">-ResourceGroupName</span></span>
<span data-ttu-id="5eedd-139">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="5eedd-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="5eedd-140">-Sku</span></span>
<span data-ttu-id="5eedd-141">Nome dell'USK per il server.</span><span class="sxs-lookup"><span data-stu-id="5eedd-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="5eedd-142">I valori supportati sono 0',' s 1',' s 2',' s 4',' s 8',' s 9',' s 8V2',' s 9V2' per il livello standard; ' B1',' B2' per il livello di base è da 1' per il livello di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="5eedd-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="5eedd-143">-Tag</span></span>
<span data-ttu-id="5eedd-144">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="5eedd-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eedd-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5eedd-145">-Confirm</span></span>
<span data-ttu-id="5eedd-146">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="5eedd-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="5eedd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eedd-147">-WhatIf</span></span>
<span data-ttu-id="5eedd-148">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="5eedd-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="5eedd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eedd-149">CommonParameters</span></span>
<span data-ttu-id="5eedd-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eedd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eedd-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eedd-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eedd-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5eedd-152">INPUTS</span></span>

### <span data-ttu-id="5eedd-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5eedd-153">System.String</span></span>

### <span data-ttu-id="5eedd-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5eedd-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5eedd-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5eedd-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5eedd-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5eedd-156">System.Int32</span></span>

### <span data-ttu-id="5eedd-157">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="5eedd-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="5eedd-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5eedd-158">OUTPUTS</span></span>

### <span data-ttu-id="5eedd-159">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5eedd-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="5eedd-160">Note</span><span class="sxs-lookup"><span data-stu-id="5eedd-160">NOTES</span></span>
<span data-ttu-id="5eedd-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="5eedd-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="5eedd-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5eedd-162">RELATED LINKS</span></span>

[<span data-ttu-id="5eedd-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5eedd-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="5eedd-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5eedd-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)

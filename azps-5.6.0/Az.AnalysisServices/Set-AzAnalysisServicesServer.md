---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: b39da37f41e3a18bc70f25fe36d67301e49867c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959309"
---
# <span data-ttu-id="0978d-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0978d-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="0978d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0978d-102">SYNOPSIS</span></span>
<span data-ttu-id="0978d-103">Modifica un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0978d-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="0978d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0978d-104">SYNTAX</span></span>

### <span data-ttu-id="0978d-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0978d-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0978d-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="0978d-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0978d-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="0978d-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0978d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0978d-108">DESCRIPTION</span></span>
<span data-ttu-id="0978d-109">Il cmdlet Set-AzAnalysisServicesServer modifica un'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0978d-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="0978d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0978d-110">EXAMPLES</span></span>

### <span data-ttu-id="0978d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0978d-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="0978d-112">Modifica il server denominato testserver nel gruppo di test del gruppo di risorse in modo da impostare i tag key1:value1 e key2:value2 e administrator su testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0978d-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="0978d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0978d-113">PARAMETERS</span></span>

### <span data-ttu-id="0978d-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="0978d-114">-Administrator</span></span>
<span data-ttu-id="0978d-115">Stringa che rappresenta un elenco di utenti o gruppi separati da virgola da impostare come amministratori nel server.</span><span class="sxs-lookup"><span data-stu-id="0978d-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="0978d-116">È necessario che per gli utenti o i gruppi sia specificato il formato UPN, ad esempio user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0978d-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="0978d-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="0978d-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="0978d-118">Uri del contenitore BLOB per il backup del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0978d-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="0978d-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="0978d-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="0978d-120">Modalità di connessione predefinita di un server del servizio di analisi</span><span class="sxs-lookup"><span data-stu-id="0978d-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="0978d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0978d-121">-DefaultProfile</span></span>
<span data-ttu-id="0978d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0978d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0978d-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="0978d-123">-DisableBackup</span></span>
<span data-ttu-id="0978d-124">Opzione per disabilitare il contenitore BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="0978d-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="0978d-125">Per abilitare di nuovo il contenitore BLOB di backup, specificare URI del contenitore BLOB di backup come -BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="0978d-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="0978d-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="0978d-126">-DisassociateGateway</span></span>
<span data-ttu-id="0978d-127">Disassociare una risorsa Gateway da un server Disassociato</span><span class="sxs-lookup"><span data-stu-id="0978d-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="0978d-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="0978d-128">-FirewallConfig</span></span>
<span data-ttu-id="0978d-129">Configurazione del firewall di un server Analysis</span><span class="sxs-lookup"><span data-stu-id="0978d-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="0978d-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="0978d-130">-GatewayResourceId</span></span>
<span data-ttu-id="0978d-131">ID di risorsa del gateway da associare a un server Analysis</span><span class="sxs-lookup"><span data-stu-id="0978d-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="0978d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="0978d-132">-Name</span></span>
<span data-ttu-id="0978d-133">Nome del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0978d-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="0978d-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0978d-134">-PassThru</span></span>
<span data-ttu-id="0978d-135">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="0978d-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="0978d-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0978d-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="0978d-137">Numero di replica di sola lettura di un server del servizio di analisi</span><span class="sxs-lookup"><span data-stu-id="0978d-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="0978d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0978d-138">-ResourceGroupName</span></span>
<span data-ttu-id="0978d-139">Nome del gruppo di risorse di Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="0978d-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="0978d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="0978d-140">-Sku</span></span>
<span data-ttu-id="0978d-141">Nome della SKU per il server.</span><span class="sxs-lookup"><span data-stu-id="0978d-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="0978d-142">I valori supportati sono "S0", "S1", "S2", "S4", "S8", "S9", "S8v2", "S9v2" per il livello Standard; "B1", "B2" per il livello Base e "D1" per il livello di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="0978d-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="0978d-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="0978d-143">-Tag</span></span>
<span data-ttu-id="0978d-144">Coppie chiave-valore sotto forma di tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="0978d-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="0978d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0978d-145">-Confirm</span></span>
<span data-ttu-id="0978d-146">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="0978d-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0978d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0978d-147">-WhatIf</span></span>
<span data-ttu-id="0978d-148">Descrive le azioni che l'operazione corrente eseguirà senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="0978d-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0978d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0978d-149">CommonParameters</span></span>
<span data-ttu-id="0978d-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0978d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0978d-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0978d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0978d-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="0978d-152">INPUTS</span></span>

### <span data-ttu-id="0978d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0978d-153">System.String</span></span>

### <span data-ttu-id="0978d-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0978d-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0978d-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0978d-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0978d-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0978d-156">System.Int32</span></span>

### <span data-ttu-id="0978d-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="0978d-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="0978d-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0978d-158">OUTPUTS</span></span>

### <span data-ttu-id="0978d-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0978d-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="0978d-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="0978d-160">NOTES</span></span>
<span data-ttu-id="0978d-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="0978d-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="0978d-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0978d-162">RELATED LINKS</span></span>

[<span data-ttu-id="0978d-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0978d-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="0978d-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0978d-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)

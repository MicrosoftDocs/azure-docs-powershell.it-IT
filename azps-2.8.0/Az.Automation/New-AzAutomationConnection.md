---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: 2b57d4d39ccce5b91a3dd8b34a42ec714b385a71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675759"
---
# <span data-ttu-id="9eaf4-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9eaf4-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="9eaf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9eaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="9eaf4-103">Crea una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="9eaf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9eaf4-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eaf4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eaf4-105">DESCRIPTION</span></span>
<span data-ttu-id="9eaf4-106">Il cmdlet **New-AzAutomationConnection** crea una connessione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="9eaf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9eaf4-107">EXAMPLES</span></span>

### <span data-ttu-id="9eaf4-108">Esempio 1: creare una connessione per ConnectionTypeName = Azure</span><span class="sxs-lookup"><span data-stu-id="9eaf4-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9eaf4-109">Il primo comando assegna una tabella hash di valori di campo alla variabile $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="9eaf4-110">Il secondo comando crea una connessione Azure denominata Connection12 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="9eaf4-111">Il comando usa i valori dei campi di connessione in $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="9eaf4-112">Esempio 2: creare una connessione per ConnectionTypeName = AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9eaf4-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9eaf4-113">Il comando crea una connessione Azure denominata Connection13 nell'account di automazione denominata AutomationAccount01 usando $RunAsAccountConnectionFieldValues e ConnectionTypeName = AzureServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="9eaf4-114">Questo ConnectionTypeName = AzureServicePrincipal viene usato principalmente per l'account di Azure Run As.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="9eaf4-115">Esempio 3: creare una connessione per ConnectionTypeName = AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="9eaf4-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9eaf4-116">Il comando crea una connessione Azure denominata Connection14 nell'account di automazione denominata AutomationAccount01 usando $ClassicRunAsAccountConnectionFieldValues e ConnectionTypeName = AzureClassicCertificate.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="9eaf4-117">Questo ConnectionTypeName = AzureClassicCertificate viene usato principalmente per l'account di Azure Classic Run As.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="9eaf4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9eaf4-118">PARAMETERS</span></span>

### <span data-ttu-id="9eaf4-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9eaf4-119">-AutomationAccountName</span></span>
<span data-ttu-id="9eaf4-120">Specifica il nome dell'account di automazione per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="9eaf4-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="9eaf4-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="9eaf4-122">Specifica una tabella hash che contiene coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="9eaf4-123">Le chiavi rappresentano i campi di connessione per il tipo di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="9eaf4-124">I valori rappresentano i valori specifici di ogni campo di connessione per l'istanza di connessione.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-124">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eaf4-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9eaf4-125">-ConnectionTypeName</span></span>
<span data-ttu-id="9eaf4-126">Specifica il nome del tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="9eaf4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eaf4-127">-DefaultProfile</span></span>
<span data-ttu-id="9eaf4-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9eaf4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eaf4-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eaf4-129">-Description</span></span>
<span data-ttu-id="9eaf4-130">Specifica una descrizione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="9eaf4-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="9eaf4-131">-Name</span></span>
<span data-ttu-id="9eaf4-132">Specifica un nome per la connessione.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="9eaf4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eaf4-133">-ResourceGroupName</span></span>
<span data-ttu-id="9eaf4-134">Specifica il nome del gruppo di risorse per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="9eaf4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eaf4-135">CommonParameters</span></span>
<span data-ttu-id="9eaf4-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eaf4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eaf4-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eaf4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eaf4-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9eaf4-138">INPUTS</span></span>

### <span data-ttu-id="9eaf4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9eaf4-139">System.String</span></span>

### <span data-ttu-id="9eaf4-140">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9eaf4-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="9eaf4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9eaf4-141">OUTPUTS</span></span>

### <span data-ttu-id="9eaf4-142">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="9eaf4-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9eaf4-143">Note</span><span class="sxs-lookup"><span data-stu-id="9eaf4-143">NOTES</span></span>

## <span data-ttu-id="9eaf4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9eaf4-144">RELATED LINKS</span></span>

[<span data-ttu-id="9eaf4-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9eaf4-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="9eaf4-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9eaf4-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


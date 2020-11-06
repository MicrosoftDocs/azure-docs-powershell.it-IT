---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: e86e25cb4752bf6899e1a00fcbccb596b64f8482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513964"
---
# <span data-ttu-id="7eb00-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7eb00-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="7eb00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eb00-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb00-103">Crea una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="7eb00-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eb00-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eb00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eb00-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb00-106">Il cmdlet **New-AzureRmAutomationConnection** crea una connessione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7eb00-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="7eb00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eb00-107">EXAMPLES</span></span>

### <span data-ttu-id="7eb00-108">Esempio 1: creare una connessione</span><span class="sxs-lookup"><span data-stu-id="7eb00-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="7eb00-109">Il primo comando assegna una tabella hash di valori di campo alla variabile $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="7eb00-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="7eb00-110">Il secondo comando crea una connessione Azure denominata Connection12 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="7eb00-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="7eb00-111">Il comando usa i valori dei campi di connessione in $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="7eb00-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="7eb00-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eb00-112">PARAMETERS</span></span>

### <span data-ttu-id="7eb00-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7eb00-113">-AutomationAccountName</span></span>
<span data-ttu-id="7eb00-114">Specifica il nome dell'account di automazione per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="7eb00-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="7eb00-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="7eb00-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="7eb00-116">Specifica una tabella hash che contiene coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="7eb00-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="7eb00-117">Le chiavi rappresentano i campi di connessione per il tipo di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="7eb00-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="7eb00-118">I valori rappresentano i valori specifici di ogni campo di connessione per l'istanza di connessione.</span><span class="sxs-lookup"><span data-stu-id="7eb00-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="7eb00-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="7eb00-119">-ConnectionTypeName</span></span>
<span data-ttu-id="7eb00-120">Specifica il nome del tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="7eb00-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="7eb00-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb00-121">-DefaultProfile</span></span>
<span data-ttu-id="7eb00-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7eb00-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7eb00-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eb00-123">-Description</span></span>
<span data-ttu-id="7eb00-124">Specifica una descrizione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="7eb00-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="7eb00-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7eb00-125">-Name</span></span>
<span data-ttu-id="7eb00-126">Specifica un nome per la connessione.</span><span class="sxs-lookup"><span data-stu-id="7eb00-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="7eb00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb00-127">-ResourceGroupName</span></span>
<span data-ttu-id="7eb00-128">Specifica il nome del gruppo di risorse per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="7eb00-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="7eb00-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb00-129">CommonParameters</span></span>
<span data-ttu-id="7eb00-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb00-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb00-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb00-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb00-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eb00-132">INPUTS</span></span>

### <span data-ttu-id="7eb00-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb00-133">System.String</span></span>

### <span data-ttu-id="7eb00-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="7eb00-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="7eb00-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eb00-135">OUTPUTS</span></span>

### <span data-ttu-id="7eb00-136">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="7eb00-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="7eb00-137">Note</span><span class="sxs-lookup"><span data-stu-id="7eb00-137">NOTES</span></span>

## <span data-ttu-id="7eb00-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eb00-138">RELATED LINKS</span></span>

[<span data-ttu-id="7eb00-139">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7eb00-139">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="7eb00-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="7eb00-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)



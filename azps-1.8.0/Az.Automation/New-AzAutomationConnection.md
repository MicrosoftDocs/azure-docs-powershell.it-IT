---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685035"
---
# <span data-ttu-id="13d97-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="13d97-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="13d97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13d97-102">SYNOPSIS</span></span>
<span data-ttu-id="13d97-103">Crea una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="13d97-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="13d97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13d97-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13d97-105">DESCRIPTION</span></span>
<span data-ttu-id="13d97-106">Il cmdlet **New-AzAutomationConnection** crea una connessione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="13d97-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="13d97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13d97-107">EXAMPLES</span></span>

### <span data-ttu-id="13d97-108">Esempio 1: creare una connessione</span><span class="sxs-lookup"><span data-stu-id="13d97-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="13d97-109">Il primo comando assegna una tabella hash di valori di campo alla variabile $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="13d97-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="13d97-110">Il secondo comando crea una connessione Azure denominata Connection12 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="13d97-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="13d97-111">Il comando usa i valori dei campi di connessione in $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="13d97-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="13d97-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13d97-112">PARAMETERS</span></span>

### <span data-ttu-id="13d97-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13d97-113">-AutomationAccountName</span></span>
<span data-ttu-id="13d97-114">Specifica il nome dell'account di automazione per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="13d97-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="13d97-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="13d97-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="13d97-116">Specifica una tabella hash che contiene coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="13d97-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="13d97-117">Le chiavi rappresentano i campi di connessione per il tipo di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="13d97-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="13d97-118">I valori rappresentano i valori specifici di ogni campo di connessione per l'istanza di connessione.</span><span class="sxs-lookup"><span data-stu-id="13d97-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="13d97-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="13d97-119">-ConnectionTypeName</span></span>
<span data-ttu-id="13d97-120">Specifica il nome del tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="13d97-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="13d97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d97-121">-DefaultProfile</span></span>
<span data-ttu-id="13d97-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="13d97-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13d97-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="13d97-123">-Description</span></span>
<span data-ttu-id="13d97-124">Specifica una descrizione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="13d97-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="13d97-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="13d97-125">-Name</span></span>
<span data-ttu-id="13d97-126">Specifica un nome per la connessione.</span><span class="sxs-lookup"><span data-stu-id="13d97-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="13d97-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d97-127">-ResourceGroupName</span></span>
<span data-ttu-id="13d97-128">Specifica il nome del gruppo di risorse per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="13d97-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="13d97-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d97-129">CommonParameters</span></span>
<span data-ttu-id="13d97-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13d97-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d97-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d97-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d97-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13d97-132">INPUTS</span></span>

### <span data-ttu-id="13d97-133">System. String</span><span class="sxs-lookup"><span data-stu-id="13d97-133">System.String</span></span>

### <span data-ttu-id="13d97-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="13d97-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="13d97-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13d97-135">OUTPUTS</span></span>

### <span data-ttu-id="13d97-136">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="13d97-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="13d97-137">Note</span><span class="sxs-lookup"><span data-stu-id="13d97-137">NOTES</span></span>

## <span data-ttu-id="13d97-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13d97-138">RELATED LINKS</span></span>

[<span data-ttu-id="13d97-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="13d97-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="13d97-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="13d97-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)



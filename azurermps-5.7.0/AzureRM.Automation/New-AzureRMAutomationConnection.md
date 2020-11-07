---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: 821453e31637f404008293679d6a63356d6f2ccd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685503"
---
# <span data-ttu-id="f3ef4-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f3ef4-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="f3ef4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ef4-103">Crea una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3ef4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3ef4-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3ef4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ef4-106">Il cmdlet **New-AzureRmAutomationConnection** crea una connessione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="f3ef4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3ef4-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ef4-108">Esempio 1: creare una connessione</span><span class="sxs-lookup"><span data-stu-id="f3ef4-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="f3ef4-109">Il primo comando assegna una tabella hash di valori di campo alla variabile $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>

<span data-ttu-id="f3ef4-110">Il secondo comando crea una connessione Azure denominata Connection12 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="f3ef4-111">Il comando usa i valori dei campi di connessione in $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="f3ef4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3ef4-112">PARAMETERS</span></span>

### <span data-ttu-id="f3ef4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3ef4-113">-AutomationAccountName</span></span>
<span data-ttu-id="f3ef4-114">Specifica il nome dell'account di automazione per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef4-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="f3ef4-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="f3ef4-116">Specifica una tabella hash che contiene coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="f3ef4-117">Le chiavi rappresentano i campi di connessione per il tipo di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="f3ef4-118">I valori rappresentano i valori specifici di ogni campo di connessione per l'istanza di connessione.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef4-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="f3ef4-119">-ConnectionTypeName</span></span>
<span data-ttu-id="f3ef4-120">Specifica il nome del tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-120">Specifies the name of the connection type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ef4-121">-DefaultProfile</span></span>
<span data-ttu-id="f3ef4-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f3ef4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef4-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3ef4-123">-Description</span></span>
<span data-ttu-id="f3ef4-124">Specifica una descrizione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-124">Specifies a description for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3ef4-125">-Name</span></span>
<span data-ttu-id="f3ef4-126">Specifica un nome per la connessione.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-126">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ef4-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3ef4-128">Specifica il nome del gruppo di risorse per cui questo cmdlet crea una connessione.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ef4-129">CommonParameters</span></span>
<span data-ttu-id="f3ef4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ef4-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ef4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ef4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3ef4-132">INPUTS</span></span>

### <span data-ttu-id="f3ef4-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f3ef4-133">None</span></span>
<span data-ttu-id="f3ef4-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f3ef4-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3ef4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3ef4-135">OUTPUTS</span></span>

### <span data-ttu-id="f3ef4-136">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="f3ef4-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="f3ef4-137">Note</span><span class="sxs-lookup"><span data-stu-id="f3ef4-137">NOTES</span></span>

## <span data-ttu-id="f3ef4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3ef4-138">RELATED LINKS</span></span>

[<span data-ttu-id="f3ef4-139">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f3ef4-139">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="f3ef4-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f3ef4-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)



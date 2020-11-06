---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: 30f88139bcd96f08dcb1c1263f5b5b5d1e35d4d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519938"
---
# <span data-ttu-id="82d6f-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="82d6f-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="82d6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="82d6f-103">Modifica una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="82d6f-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82d6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82d6f-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82d6f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="82d6f-106">Il cmdlet **set-AzureRmAutomationCredential** modifica una credenziale come oggetto **PSCredential** in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="82d6f-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="82d6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="82d6f-108">Esempio 1: aggiornare una credenziale</span><span class="sxs-lookup"><span data-stu-id="82d6f-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="82d6f-109">Il primo comando assegna un nome utente alla variabile $User.</span><span class="sxs-lookup"><span data-stu-id="82d6f-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="82d6f-110">Il secondo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="82d6f-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="82d6f-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="82d6f-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="82d6f-112">Il terzo comando crea una credenziale basata su $User e $Password e quindi la archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="82d6f-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="82d6f-113">Il comando finale modifica le credenziali di automazione denominate ContosoCredential per l'utilizzo delle credenziali in $Credential.</span><span class="sxs-lookup"><span data-stu-id="82d6f-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="82d6f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82d6f-114">PARAMETERS</span></span>

### <span data-ttu-id="82d6f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82d6f-115">-AutomationAccountName</span></span>
<span data-ttu-id="82d6f-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica una credenziale.</span><span class="sxs-lookup"><span data-stu-id="82d6f-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="82d6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d6f-117">-DefaultProfile</span></span>
<span data-ttu-id="82d6f-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="82d6f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82d6f-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="82d6f-119">-Description</span></span>
<span data-ttu-id="82d6f-120">Specifica una descrizione per le credenziali modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82d6f-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="82d6f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="82d6f-121">-Name</span></span>
<span data-ttu-id="82d6f-122">Specifica il nome delle credenziali modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82d6f-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="82d6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="82d6f-124">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica una credenziale.</span><span class="sxs-lookup"><span data-stu-id="82d6f-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="82d6f-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="82d6f-125">-Value</span></span>
<span data-ttu-id="82d6f-126">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="82d6f-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82d6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d6f-127">CommonParameters</span></span>
<span data-ttu-id="82d6f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d6f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82d6f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d6f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82d6f-130">INPUTS</span></span>

### <span data-ttu-id="82d6f-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82d6f-131">None</span></span>
<span data-ttu-id="82d6f-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="82d6f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82d6f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82d6f-133">OUTPUTS</span></span>

### <span data-ttu-id="82d6f-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="82d6f-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="82d6f-135">Note</span><span class="sxs-lookup"><span data-stu-id="82d6f-135">NOTES</span></span>

## <span data-ttu-id="82d6f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82d6f-136">RELATED LINKS</span></span>

[<span data-ttu-id="82d6f-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="82d6f-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="82d6f-138">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="82d6f-138">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="82d6f-139">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="82d6f-139">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)



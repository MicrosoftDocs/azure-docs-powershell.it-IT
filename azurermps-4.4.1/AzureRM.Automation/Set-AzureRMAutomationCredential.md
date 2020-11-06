---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: e2a461666edf4f06e78f2bc97f47fcb63ab1c19a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511371"
---
# <span data-ttu-id="92018-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="92018-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="92018-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92018-102">SYNOPSIS</span></span>
<span data-ttu-id="92018-103">Modifica una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="92018-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92018-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92018-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92018-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92018-105">DESCRIPTION</span></span>
<span data-ttu-id="92018-106">Il cmdlet **set-AzureRmAutomationCredential** modifica una credenziale come oggetto **PSCredential** in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="92018-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="92018-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92018-107">EXAMPLES</span></span>

### <span data-ttu-id="92018-108">Esempio 1: aggiornare una credenziale</span><span class="sxs-lookup"><span data-stu-id="92018-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="92018-109">Il primo comando assegna un nome utente alla variabile $User.</span><span class="sxs-lookup"><span data-stu-id="92018-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="92018-110">Il secondo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="92018-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="92018-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="92018-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="92018-112">Il terzo comando crea una credenziale basata su $User e $Password e quindi la archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="92018-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="92018-113">Il comando finale modifica le credenziali di automazione denominate ContosoCredential per l'utilizzo delle credenziali in $Credential.</span><span class="sxs-lookup"><span data-stu-id="92018-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="92018-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92018-114">PARAMETERS</span></span>

### <span data-ttu-id="92018-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="92018-115">-AutomationAccountName</span></span>
<span data-ttu-id="92018-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica una credenziale.</span><span class="sxs-lookup"><span data-stu-id="92018-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="92018-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="92018-117">-Description</span></span>
<span data-ttu-id="92018-118">Specifica una descrizione per le credenziali modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92018-118">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="92018-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="92018-119">-Name</span></span>
<span data-ttu-id="92018-120">Specifica il nome delle credenziali modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92018-120">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="92018-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92018-121">-ResourceGroupName</span></span>
<span data-ttu-id="92018-122">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica una credenziale.</span><span class="sxs-lookup"><span data-stu-id="92018-122">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="92018-123">-Valore</span><span class="sxs-lookup"><span data-stu-id="92018-123">-Value</span></span>
<span data-ttu-id="92018-124">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="92018-124">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92018-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92018-125">-DefaultProfile</span></span>
<span data-ttu-id="92018-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92018-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92018-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92018-127">CommonParameters</span></span>
<span data-ttu-id="92018-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92018-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92018-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92018-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92018-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92018-130">INPUTS</span></span>

## <span data-ttu-id="92018-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92018-131">OUTPUTS</span></span>

### <span data-ttu-id="92018-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="92018-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="92018-133">Note</span><span class="sxs-lookup"><span data-stu-id="92018-133">NOTES</span></span>

## <span data-ttu-id="92018-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92018-134">RELATED LINKS</span></span>

[<span data-ttu-id="92018-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="92018-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="92018-136">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="92018-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="92018-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="92018-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)



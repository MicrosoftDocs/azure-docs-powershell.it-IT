---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023488"
---
# <span data-ttu-id="fa43c-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fa43c-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="fa43c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa43c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa43c-103">Ottiene le impostazioni dell'agente IaaS di SQL Server in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fa43c-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="fa43c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa43c-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fa43c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa43c-105">DESCRIPTION</span></span>
<span data-ttu-id="fa43c-106">Il cmdlet **Get-AzureVMSqlServerExtension** ottiene le impostazioni dell'agente di SQL Server come servizio (IaaS) in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fa43c-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="fa43c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa43c-107">EXAMPLES</span></span>

### <span data-ttu-id="fa43c-108">Esempio 1: ottenere le impostazioni di un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fa43c-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="fa43c-109">Ottiene le impostazioni dell'estensione di SQL Server in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fa43c-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="fa43c-110">Esempio 2: ottenere le impostazioni di un agente di IaaS di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fa43c-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="fa43c-111">Ottiene le impostazioni dell'agente IaaS di SQL Server in una particolare macchina virtuale usando l'input tramite pipe.</span><span class="sxs-lookup"><span data-stu-id="fa43c-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="fa43c-112">Esempio 3: ottenere le impostazioni di un agente IaaS della versione specifica di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fa43c-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="fa43c-113">Questo comando consente di ottenere le impostazioni della versione specifica di agente IaaS di SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fa43c-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="fa43c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa43c-114">PARAMETERS</span></span>

### <span data-ttu-id="fa43c-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fa43c-115">-InformationAction</span></span>
<span data-ttu-id="fa43c-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="fa43c-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fa43c-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa43c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa43c-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="fa43c-118">Continue</span></span>
- <span data-ttu-id="fa43c-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="fa43c-119">Ignore</span></span>
- <span data-ttu-id="fa43c-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="fa43c-120">Inquire</span></span>
- <span data-ttu-id="fa43c-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fa43c-121">SilentlyContinue</span></span>
- <span data-ttu-id="fa43c-122">Stop</span><span class="sxs-lookup"><span data-stu-id="fa43c-122">Stop</span></span>
- <span data-ttu-id="fa43c-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="fa43c-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa43c-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fa43c-124">-InformationVariable</span></span>
<span data-ttu-id="fa43c-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="fa43c-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa43c-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="fa43c-126">-Profile</span></span>
<span data-ttu-id="fa43c-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa43c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa43c-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="fa43c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa43c-129">-VM</span><span class="sxs-lookup"><span data-stu-id="fa43c-129">-VM</span></span>
<span data-ttu-id="fa43c-130">Specifica l'oggetto macchina virtuale persistente da cui vengono recuperate le impostazioni da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa43c-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa43c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa43c-131">CommonParameters</span></span>
<span data-ttu-id="fa43c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa43c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa43c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa43c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa43c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa43c-134">INPUTS</span></span>

## <span data-ttu-id="fa43c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa43c-135">OUTPUTS</span></span>

## <span data-ttu-id="fa43c-136">Note</span><span class="sxs-lookup"><span data-stu-id="fa43c-136">NOTES</span></span>

## <span data-ttu-id="fa43c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa43c-137">RELATED LINKS</span></span>

[<span data-ttu-id="fa43c-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fa43c-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="fa43c-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fa43c-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


